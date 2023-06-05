<script lang="ts">
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    
    export let modalOpen: boolean = false;

    const toggleModal = () => dispatch("toggleModal");
</script>

{ #if modalOpen }
    <div id="backdrop">
        <div id="modal">
            <slot></slot>
        </div>
    </div>
{ /if }