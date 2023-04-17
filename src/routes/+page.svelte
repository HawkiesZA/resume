<script>
    import Header from './header.svelte'
    import Experience from './experience.svelte';
    import { employmentHistory } from './employmentHistory.js'
    import { educationHistory } from './educationHistory.js'
</script>

<div class="card">
    <div class="container">
        <Header />
        
        <div class="content">
            <h2>Employment History</h2>
            {#each employmentHistory as item}
                <Experience
                    title = {item.title}
                    monthYearStart = {item.start}
                    monthYearEnd = {item.end}
                    description = {item.description}
                />
            {/each}
        
        
            <h2>Education</h2>
            {#each educationHistory as item}
                <Experience
                    title = {item.title}
                    monthYearStart = {item.start}
                    monthYearEnd = {item.end}
                    description = {item.description}
                />
            {/each}
        </div>
    </div>
</div>

<style>
    .card {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
    }

    .container {
        padding: 2px 16px;
    }

    .content {
        margin: auto;
        width: 50%;
        padding: 10px;
    }

    h2 {
        text-align: center;
        font-family: Arial, Helvetica, sans-serif
    }

    
</style>