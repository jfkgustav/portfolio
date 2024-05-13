<script lang="ts">
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import jointfly_start from '$lib/assets/jointfly_start.png';
	import jointfly_play from '$lib/assets/jointfly_play.png';
	import recharge from '$lib/assets/recharge.png';
	import three_d_studio_one from '$lib/assets/3d_studio_one.png';
	import three_d_parallel from '$lib/assets/3d_parallel.png';
	import three_d_oblique from '$lib/assets/3d_oblique.png';
	import skrivert_meme from '$lib/assets/skrivert_meme.jpg';
	import AspectRatio from '$lib/components/ui/aspect-ratio/aspect-ratio.svelte';
</script>

<div class="overflow-y-scroll snap-y snap-mandatory sm:-mt-10">
	<!--
  <h1 class="scroll-m-20 text-3xl sm:text-orange-800 sm:text-4xl font-extrabold text-center sm:pb-5 tracking-tight ">
    Mina projekt
  </h1>

  <h3 class="sm:hidden scroll-m-20 text-sm text-center tracking-tight pb-5 text-gray-500">
    Swipea för att se fler bilder
  </h3>
      !-->

	<div class="h-screen snap-center items-center sm:grid sm:grid-cols-2" id="jointfly">
		<div class="container snap-center pb-10 sm:order-2" id="jointfly right">
			<Carousel.Root
				opts={{
					align: 'start',
					loop: true
				}}
			>
				<Carousel.Content class="mx-auto">
					<Carousel.Item>
						<p class="py-3 text-center text-md font-semibold leading-none">1 / 2</p>
						<img src={jointfly_start} alt="jointfly startskärm" class="mx-auto w-full sm:w-5/6" />
						<p class="py-3 text-center text-md font-semibold leading-none">jointflys startskärm</p>
					</Carousel.Item>
					<Carousel.Item>
						<p class="py-3 text-center text-md font-semibold leading-none">2 / 2</p>
						<img src={jointfly_play} alt="jointfly körs" class="mx-auto w-full sm:w-5/6" />
						<p class="py-3 text-center text-md font-semibold leading-none">
							Bild på när jointfly körs
						</p>
					</Carousel.Item>
				</Carousel.Content>
				<Carousel.Previous class="hidden " />
				<Carousel.Next class="hidden " />
			</Carousel.Root>
		</div>

		<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="jointfly left">
			<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
				jointfly!
			</h1>

			<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
				En prototyp av en app gjord för att styra flera drönare samtidigt från en mobil enhet.
			</h3>

			<div class="flex py-3 justify-between w-3/4 sm:w-full mx-auto text-sm font-bold text-gray-700 sm:text-left sm:text-xl">
				<p>Figma</p> <p>Användarstudier</p> <p>Prototyping</p>
			</div>


			<p class="text-sm py-3 text-center text-blue-500 font-semibold sm:text-left sm:text-xl"><a href="/jointfly" >
				Läs mer
			</a></p>


		</div>
	</div>

	<div class="h-screen snap-center items-center sm:grid sm:grid-cols-2 sm:px-5" id="grafikmotor">
		<div class="sm:container sm:order-2" id="grafikmotor right">
			<div class="container">
				<Carousel.Root
					opts={{
						align: 'start',
						loop: true
					}}
				>
					<Carousel.Content class="mx-auto">
						<Carousel.Item>
							<p class="py-3 text-center text-md font-semibold leading-none">1 / 3</p>
							<img
								src={three_d_studio_one}
								alt="3D studio bild 1"
								class="mx-auto w-full border border border-2 sm:w-5/6"
							/>
							<p class="py-3 text-center text-md font-semibold leading-none">3D Studio</p>
						</Carousel.Item>
						<Carousel.Item>
							<p class="py-3 text-center text-md font-semibold leading-none">2 / 3</p>
							<img
								src={three_d_parallel}
								alt="Parallel Projektion"
								class="mx-auto w-full border sm:w-5/6"
							/>
							<p class="py-3 text-center text-md font-semibold leading-none">Parallel Projection</p>
						</Carousel.Item>
						<Carousel.Item>
							<p class="py-3 text-center text-md font-semibold leading-none">3 / 3</p>
							<img
								src={three_d_oblique}
								alt="Oblik Projektion"
								class="mx-auto w-full border sm:w-5/6"
							/>
							<p class="py-3 text-center text-md font-semibold leading-none">Oblique Projection</p>
						</Carousel.Item>
					</Carousel.Content>
					<Carousel.Previous class="hidden" />
					<Carousel.Next class="hidden" />
				</Carousel.Root>
			</div>
		</div>

		<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="grafikmotor left">
			<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
				3D Studio
			</h1>

			<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
				Simpel grafikmotor skriven i C++ med hjälp av OpenGL, GLM och tinyOBJloader
			</h3>

			<div class="flex py-3 justify-between w-3/4 sm:w-full mx-auto text-sm font-bold text-gray-700 sm:text-left sm:text-xl">
				<p>C++</p> <p>OpenGL</p> <p>Datorgrafik</p>
			</div>


			<p class="text-sm py-3 text-center text-blue-500 font-semibold sm:text-left sm:text-xl"><a href="/jointfly" >
				Läs mer
			</a></p>

		</div>
	</div>

	<div class="h-screen snap-center items-center sm:grid sm:grid-cols-2" id="recharge">
		<div class="container order-2 pb-10" id="recharge right">
			<img src={recharge} alt="recharge" class="mx-auto w-full sm:w-5/6" />
			<p class="py-3 text-center text-xl font-semibold leading-none">RECHARGE</p>
		</div>

		<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="recharge left">
			<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
				RECHARGE
			</h1>

			<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
				En prototyp av en app gjord för <br /> att smidigt hitta och boka laddstationer för elbilar
			</h3>

			<div class="flex justify-between text-sm py-3 w-full mx-auto font-bold text-gray-700 sm:text-left sm:text-xl">
				<p>Figma</p> <p>Användarstudier</p> <p>Wireframes</p> <p>Prototyping</p>
			</div>

			<p class="text-sm pt-3 text-center text-blue-500 font-semibold sm:text-left sm:text-xl"><a href="/jointfly" >
				Läs mer
			</a></p>

		</div>
	</div>

	<div class="h-screen snap-center items-center sm:grid sm:grid-cols-2" id="skrivert">
		<div class="container pb-10 sm:order-2" id="skrivert right">
			<img src={skrivert_meme} alt="skrivert meme if i had any" class="mx-auto w-1/2 sm:w-1/2" />
			<p class="py-3 text-center text-xl font-semibold leading-none">
				Än så länge har vi inte kommit så långt i detta projekt :)
			</p>
		</div>

		<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="skrivert left">
			<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
				skrivert
			</h1>

			<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
				Projekt för att skapa GUI till en textproduktionsapplikation
			</h3>

			<div class="flex justify-between w-full mx-auto text-sm py-3 font-bold text-gray-700 sm:text-left sm:text-xl">
				<p>Figma</p> <p>Svelte</p> <p>ShadCN</p> <p>Tailwind</p> <p>Design-Build-Test</p> 
			</div>


			<p class="text-sm py-3 text-center text-blue-500 font-semibold sm:text-left sm:text-xl"><a href="/jointfly" >
				Läs mer
			</a></p>
			
		</div>
	</div>
</div>
