<script lang="ts">

  import "../app.pcss";
  import { Button } from "$lib/components/ui/button";
  import * as Sheet from "$lib/components/ui/sheet";
  import hamburger from "$lib/assets/hamburgare.png";
  import { mediaQuery } from "svelte-legos";
 
 
  let open = false;
  const isDesktop = mediaQuery("(min-width: 768px)");

</script>

<div class="bg-local h-[calc(100vh)]">

  
  {#if $isDesktop}
  <div class="flex flex-wrap items-center justify-between mx-auto py-4 px-32">
    <div>
      <Button variant="link" class="font-bold text-lg" href="/">Hem</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold text-lg" href="/projects">Projekt</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold text-lg" href="/contact">Kontakt</Button>
    </div>
    <div>
      <Button variant="link" class="font-bold text-lg" href="/about">Om</Button>
    </div>
  </div>

  
  <div class="h-full"> 
   <slot />
  </div>

  
  {:else}
  <div class="text-right">
  <Sheet.Root>
    <Sheet.Trigger asChild let:builder>
      <Button builders={[builder]} variant="link" class="w-1/4 m-2 mr-0">
        <img src={hamburger} alt="meny">
      </Button>
    </Sheet.Trigger>
    <Sheet.Content side="right" class="h-1/2 w-full">
      <Sheet.Close asChild let:builder>
      <div class="text-center pt-10">
        <div>
          <Button builders={[builder]} variant="link" class="font-bold" href="/">Hem</Button>
        </div>
        <div>
          <Button builders={[builder]} variant="link" class="font-bold" href="/projects">Projekt</Button>
        </div>
        <div>
          <Button builders={[builder]} variant="link" class="font-bold" href="/contact">Kontakt</Button>
        </div>
        <div>
          <Button builders={[builder]} variant="link" class="font-bold" href="/about">Om</Button>
        </div>
      </div>
      </Sheet.Close>
      <Sheet.Footer class="items-center">
        <Sheet.Close asChild let:builder>
          <Button builders={[builder]} type="submit" class="w-1/4 font-bold" variant="ghost">X</Button>
        </Sheet.Close>
      </Sheet.Footer>
    </Sheet.Content>
  </Sheet.Root>
  </div>

  <div class="h-full"> 
    <slot />
   </div>
  {/if}
</div>
