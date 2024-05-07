<script>
import Draggable from '../plugins/Draggable.svelte';
export let projectName;

</script>

<div class="project-modal active {projectName}">
    <Draggable>
        <div class="heading">
            <span class="date">2024</span>
            <span class="domaine">UI Design</span>
        </div>
        <h1>
            {projectName}
        </h1>
    
        <img class="project-image" src="/src/lib/images/{projectName}/fond.jpg" alt="">
    
        <div class="project-presentation">
            <div class="description">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda saepe obcaecati accusantium quidem mollitia deleniti illo est harum aliquid rem eos, similique animi alias asperiores doloremque ea ullam libero at.
                </p>
    
             </div>
            <div class="team">
                <span class="team-title">Team</span>
                <span class="member">Thibaut CHAYOT</span>
                <span class="member">Audrey GODEFROY</span>
            </div>
        </div>

    </Draggable>
    
</div>



<style lang="scss">
    .project-modal {
        display: none;
        &.active {
            display: block;
        }
        .heading {
            text-transform: uppercase;
            font-size: .7rem;
            .domaine {
                &:before {
                    content:'• ';

                }
            }
        }   
        img {
			width: 100%;
		}
        .project-presentation {
            display: flex;
            .description {
                flex:70% 0 0;
                p {
                width: 78%;
                margin: 0;
                }
            }
            .team {
                .team-title {
                    opacity: .7;
                    font-variation-settings: "wght" 600;
                    display: block;
                }
                .member {
                    display: block;
                }
            }
        }
    }
</style>