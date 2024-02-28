<script>import "../app.pcss";

  import { Button } from "$lib/components/ui/button";

</script>

<div class="h-[calc(100vh)]">
  <div class="flex flex-wrap items-center justify-between mx-auto py-4 px-32">
    <div>
      <Button variant="link" class="font-bold" href="/">Hem</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold" href="/projects">Projekt</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold" href="/contact">Kontakt</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold" href="/about">Om</Button>
    </div>
  </div>

  
  <div class="h-full"> 
   <slot />
  </div>


</div>
