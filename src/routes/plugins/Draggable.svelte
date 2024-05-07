<script>
	export let left = 100;
	export let top = 100;
	let moving = false;	
	//import Project from "../components/project.svelte";

	
	function onMouseDown() {
		moving = true;
	}
	
	function onMouseMove(e) {
		if (moving) {
			left += e.movementX;
			top += e.movementY;
		}
	}
	
	function onMouseUp() {
		moving = false;
	}
	
	function close() {
		//console.log(this.parentElement.parentElement.parentElement.parentElement);
		let close = this.parentElement.parentElement.parentElement.parentElement;
		close.remove();

	}
	
// 	$: console.log(moving);
</script>

<style lang="scss">
	.draggable {
		position: fixed;
		max-width:50vw;
		background-color:red;
		z-index: 9999;
		border-radius: 15px;
		padding: 4rem 1rem 1rem 1rem;
		.topbar {
			user-select: none;
			width: calc(100% - 2rem);
			height: 30px;
			border-radius: 15px 15px 0 0;
			background-color:blue;
			position: absolute;
			top:0;
			left: 0;
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 0 1rem;
			.topbar-buttons {
				display: flex;
				gap: .5rem;
				div {
					width: 10px;
					height: 10px;
					border-radius: 50%;
					&:hover {
						cursor:pointer;
					}
					&.close {
						background-color: red;
					}
					&.hide {
						background-color:orange;
					}
					&.fullscreen {
						background-color:green;
					}
				}
			}
		}
	}
</style>

<section class="draggable" style="left: {left}px; top: {top}px;">
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<div class="topbar" on:mousedown={onMouseDown}>
		<div class="topbar-buttons">
			<div class="close" on:click={close} ></div>
			<div class="hide"></div>
			<div class="fullscreen"></div>
		</div>
		<span class="project-name">Nom du projet</span>
	</div>
	<slot></slot>
</section>

<svelte:window on:mouseup={onMouseUp} on:mousemove={onMouseMove} />