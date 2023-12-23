<script lang="ts">
    // this component is the left navbar and the top navbar when the left navbar is closed
    // im going to rework so that instead of changing menus, its going to fly out from the left and 
    // be a single menu instead of being separated, by this i mean the nav and the left menu aren't the same
    // and it will be mobile first

    // use device finder to determine what aspect ratio the screen should be using
    // basically what this does is controls how the navigation should look depending on the resolution and aspect ratio
    // the various conditions are displayed below
    // the device layouts start from small and change as they get larger
    // they also start with vertical orientations and then move to horizontal ones
    // let screen = getScreen()

    // temp win size vals
    // let width: number = window.innerWidth
    // let height: number = window.innerHeight
    // let aspectRatio = width / height
    let device = "skinny"
    // if (aspectRatio > 1) {
    //     device = "wide"
    // }
</script>

<div class="bg-black sticky top-0">
{#if device == "skinny"}
    <div class="flex flex-row">
        <img class="m-5 w-1/4" src="../../botforge_logo_1_50.webp" alt="logo">
    </div>
{/if}
</div>