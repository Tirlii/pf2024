<script>

    export let title;
    export let desc;
    export let project;
    import ProjectModal from "./project-modal.svelte";




    // function addProject() {
    //     let modal = ProjectModal;
    //     document.body.append(modal);
    //     console.log(ProjectModal);
    // }
    function addProject() {
        let projectName = this.id;
        const exists = document.getElementsByClassName(projectName);
        if(exists.length < 1) {
            const element = new ProjectModal({
                target: document.querySelector('#'+ projectName),
                props:{
                    projectName: projectName
                }
            })
        }
        //console.log(this.ProjectModal);
        //console.log(exists);
        //console.log(exists.length);
    }
    

</script>


<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<div class="project" id="{project}" style="background-image: url(/src/lib/images/{project}/fond.jpg);" on:click={addProject}>
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