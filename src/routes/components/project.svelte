<script>

    export let title;
    export let desc;
    export let project;

</script>


<div class="project" style="background-image: url(/src/lib/images/{project}/fond.jpg);">
    <span class="title">{title}</span>
    <span class="desc">{desc}</span>
</div>

<style lang="scss">
    .project {
        border-radius: 2rem;
        //background-image: url(../../lib/images/jpg/fond.jpg);
        height: 40rem;
        width: 40%;
        background-position: center;
        background-repeat:no-repeat;
        background-size: 250%;
        transition: background-size .3s;
        &:hover {
            background-size: 260%;
        }
        .title {
            font-size: 2rem;
            color: white;
            font-variation-settings: "wght" 500;
            margin: 4rem;
        }
    }
</style>