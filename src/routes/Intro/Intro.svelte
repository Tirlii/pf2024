<script>
	import pp from '$lib/images/profilepicture.jpg';
    import Otw from './Otw.svelte'
    import Cta from '../components/bouton.svelte'
</script>




<div class="intro">
    <Otw />
    <p>I’m Thibaut <img src={pp} alt="profil" class="pp"> — an <span class="bolder">interface designer</span> from Reims, focusing on <span class="bolder">building functional websites</span> that will <span class="bolder">increase conversion</span> and help <span class="bolder">reach customer</span></p>
    <Cta />
</div>



<style lang="scss">
    .intro {
        top: 40vh;
        left: 0;
        position: fixed;
        z-index: -1;
        p {
            color:#000000CC;
            font-size: 3rem;
            line-height: 3rem;
            .bolder {
                font-variation-settings: "wght" 500;
                color:#000000;
            }
            .pp {
                width: 3rem;
                height: 3rem;
                border-radius: 50%;
                vertical-align:bottom;
            }
        }   
    }
</style>