
<script>
 import {onMount} from 'svelte'
 let mobile=false;
 const handleResize=()=>{
  mobile=(window.innerWidth<1024)
 }
  onMount(()=>{
    handleResize
    window.addEventListener('resize',handleResize)
  });

  import Hmap from '$lib/assets/Hmap.png?url';
  import Vmap from '$lib/assets/Vmap.png?url'
</script>






  <div class="w-full h-full bg-black p-10 pt-20 flex flex-col md:flex-row justify-around">
        <img src={mobile?Vmap:Hmap} alt="" style="width: 100%; height: auto;">
    </div>

  
  
