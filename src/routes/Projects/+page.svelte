<script>

</script>

<div class="project">

    <span class="date">2024</span>
    <span class="domaine">UI Design</span>

    <img class="project-image" src="/src/lib/images/jpg/fond.jpg" alt="">

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

</div>


<style lang="scss">

    .project {
        .project-image {
            width:100%;
            max-height:50vh;
            object-fit: cover;
            object-position: top;
            border-radius: 50px;
        }
        .project-presentation {
            display: flex;
            gap: 10%;
            .description {
                flex:70% 0 0;
                p {
                width: 70%;
                }
            }
            .team {
                flex: 30% 0 0;
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
