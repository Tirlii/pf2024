<script>
    import Project from "./project.svelte"
</script>

<div class="projectList">
    <Project 
    title="Jean Paul Gaultier"
    desc=""
    project="jpg"
    />
    <Project 
    title="Resonate"
    desc=""
    project="resonate"
    />
    <Project 
    title="A2JOB"
    desc=""
    project="A2JOB"
    />
    <Project 
    title="Onze Metres Carrés"
    desc=""
    project="omc"
    />
    <Project 
    title="La Réclame"
    desc=""
    project="lareclame"
    />


</div>



<style lang="scss">
    .projectList {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem;
        justify-content: center;
        backdrop-filter: blur(1rem);
        margin-top: 80vh;
        padding-top:1rem;
    }

</style>