<script lang="ts">
	import avatar from '$lib/assets/portfolio_bild.jpg';
	import linkedin from '$lib/assets/linkedin.png';
	import cv from '$lib/assets/cv.png';
	import * as Avatar from '$lib/components/ui/avatar';
	import cv_file from '$lib/assets/CV.pdf';
	import gitHub from '$lib/assets/Github.png';
	import epic from '$lib/assets/epic.png';
	import epic_square from '$lib/assets/epic_square.png';
	import * as Carousel from '$lib/components/ui/carousel/index.js';
	import jointfly_start from '$lib/assets/jointfly_start.png';
	import recharge from '$lib/assets/recharge.png';
	import three_d_studio_one from '$lib/assets/three_d_studio_one.png';
	import jointfly_play from '$lib/assets/jointfly_play.png';
	import three_d_parallel from '$lib/assets/three_d_parallel.png';
	import three_d_oblique from '$lib/assets/three_d_oblique.png';
	import mail from '$lib/assets/mail.png';
	import skrivert_gif from '$lib/assets/skrivert_infinity.gif';
	import skrivert_settings from '$lib/assets/skrivert/settings.png';
	import skrivert_skriva from '$lib/assets/skrivert/skriva.png';
	import radioInfoMainMenu from '$lib/assets/radioInfo/mainMenu.png';
	import radioInfoP3 from '$lib/assets/radioInfo/P3.png';
	import radioInfoMore from '$lib/assets/radioInfo/moreInfo.png';

	import Autoplay from 'embla-carousel-autoplay';
	import { fullScreenAction, mediaQuery } from 'svelte-legos';
	import ImageZoom from '$lib/components/ImageZoom.svelte';

	const isDesktop = mediaQuery('(min-width: 768px)');

	let show_mail = false;

	let kontakt = {
		body: 'Kontakta mig!'
	};

	function handler() {
		show_mail = !show_mail;
		if (show_mail) {
			kontakt.body = 'jfkgustav@gmail.com';
		} else {
			kontakt.body = 'Kontakta mig!';
		}
	}

  const imageMap = {
    radioInfoMainMenu,
    radioInfoP3,
    radioInfoMore,
    skrivert_gif,
    skrivert_settings,
    skrivert_skriva,
    jointfly_start,
    jointfly_play,
    three_d_studio_one,
    three_d_parallel,
    three_d_oblique,
    recharge,
  };

	let large_img_src = '';

	function enlargeImage(id: string) {
		const image_to_enlarge = document.getElementById('large_div');
		const exit_button = document.getElementById('exit_button');
		large_img_src = imageMap[id]
		image_to_enlarge?.classList.toggle('hidden');
		exit_button?.focus();
	}
</script>

<div class="h-screen snap-y snap-mandatory overflow-y-scroll">
	<div
		class="flex h-screen w-screen snap-center justify-center gap-40 text-center sm:py-20 sm:text-left md:grid md:grid-cols-2"
		style="background-image: url({epic}); background-repeat: no-repeat; background-size: cover;"
	>
		<div class="absolute mx-auto flex justify-center drop-shadow-2xl sm:order-2 sm:hidden">
			<img src={epic_square} alt="Find bild på mig :)" class="rounded-lg object-cover" />
		</div>

		<div
			class="container z-20 my-auto mt-72 w-full rounded-lg bg-slate-100 p-5 sm:ml-32 sm:w-full sm:bg-white sm:px-10 md:static md:mt-0"
		>
			<h1 class=" text-3xl font-extrabold tracking-tight lg:text-5xl">Gustav Johansson</h1>
			<h3 class="text-lg tracking-tight text-gray-500 lg:text-2xl">
				En kille som gillar sin dator
			</h3>

			<p class="text-md py-5 text-left font-semibold tracking-tight text-gray-800 lg:text-lg">
				Jag har suttit vid datorn majoriteten av mitt liv och nu har jag även tänkt att det ska
				fortsätta så. Därför har jag valt att utbilda mig till civilingenjör i interaktion och
				design och är nu på mitt fjärde år.
			</p>

			<p class="text-md hidden font-semibold tracking-tight text-gray-800 md:inline lg:text-lg">
				Rulla ned för att lära känna mig och kika på lite grejor jag har hållit på med!
			</p>

			<div class="mt-5 flex grid-cols-3 justify-between">
				<div class=" flex flex-col items-center justify-center gap-x-3 p-0 sm:flex-row">
					<a
						href="https://drive.google.com/file/d/1FDiO_uVXU5ZW1Nz2XPv_lO5PlqxAiKji/view"
					>
						<Avatar.Root>
							<Avatar.Image src={cv} alt="Mitt CV" />
							<Avatar.Fallback>CV</Avatar.Fallback>
						</Avatar.Root>
					</a>

					<a
						href="https://drive.google.com/file/d/1FDiO_uVXU5ZW1Nz2XPv_lO5PlqxAiKji/view"
						class="text-l tracking-tight text-purple-600 lg:text-2xl"
					>
						Hämta CV
					</a>
				</div>

				<div class=" flex flex-col items-center justify-center gap-x-3 p-0 sm:flex-row">
					<Avatar.Root>
						<a href="https://github.com/jfkgustav"
							><Avatar.Image src={gitHub} alt="github logo" />
						</a>
						<Avatar.Fallback>GH</Avatar.Fallback>
					</Avatar.Root>

					<a
						href="https://github.com/jfkgustav"
						class="text-l tracking-tight text-[#0284c7] lg:text-2xl"
					>
						Github
					</a>
				</div>

				<div class=" flex flex-col items-center justify-center gap-x-3 p-0 sm:flex-row">
					<Avatar.Root>
						<button
							on:click={handler}
							class="text-l tracking-tight text-[rgb(186,199,2)] lg:text-2xl"
						>
							<Avatar.Image src={mail} alt="kontakta mig" />
						</button>
						<Avatar.Fallback>Mail</Avatar.Fallback>
					</Avatar.Root>

					{#if !show_mail}
						<button
							on:click={handler}
							class="text-l tracking-tight text-[rgb(186,199,2)] lg:text-2xl"
						>
							<pre>{kontakt.body}</pre>
						</button>
					{:else}
						<a
							href="mailto:jfkgustav@gmail.com"
							class="text-l tracking-tight text-[rgb(186,199,2)] lg:text-2xl"
						>
							<pre>{kontakt.body}</pre>
						</a>
					{/if}
				</div>
			</div>
		</div>
	</div>

	<div class="z-30 backdrop-blur-xl">
		<!--
      <h3 class="sm:hidden  text-sm text-center tracking-tight pb-5 text-gray-500">
        Swipea för att se fler bilder
      </h3>
      !-->
	<div class=" h-screen snap-center sm:pt-10" id="radioInfo">
			<h1 class="pb-16 text-center text-lg font-bold tracking-tight">Mina projekt</h1>
			<div class="container items-center justify-center sm:grid sm:grid-cols-2">
				<div class="sm:order-2" id="radioInfo right">
					<Carousel.Root
						opts={{
							align: 'start',
							loop: true
						}}
					>
						<Carousel.Content class="mx-auto">
							<Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">1 / 3</p>
								<button on:click={() => enlargeImage('radioInfoP3')}>
									<img
										src={radioInfoP3}
										alt="radioInfo visar P3s tablå"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>
								<p class="text-md py-3 text-center font-semibold leading-none">
									RadioInfo visar P3s tablå
								</p>
							</Carousel.Item>
						  <Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">2 / 3</p>
								<button on:click={() => enlargeImage('radioInfoMainMenu')}>
									<img
										src={radioInfoMainMenu}
										alt="radioInfos huvudmeny"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>

								<p class="text-md py-3 text-center font-semibold leading-none">
									Bild på RadioInfos huvudmeny.
								</p>
							</Carousel.Item>
							<Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">3 / 3</p>
								<button on:click={() => enlargeImage('radioInfoMore')}>
									<img
										src={radioInfoMore}
										alt="radioInfo visar mer info om ett program"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>
								<p class="text-md py-3 text-center font-semibold leading-none">
								  RadioInfo visar mer info om ett program
								</p>
							</Carousel.Item>
						</Carousel.Content>
						{#if $isDesktop}
							<Carousel.Previous />
							<Carousel.Next />
						{/if}
					</Carousel.Root>
				</div>

				<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="radioInfo left">
					<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
						RadioInfo
					</h1>

					<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
            Ett program som kan visa programtablån för olika kanaler från Sveriges Radio.
					</h3>

					<div
						class="mx-auto flex w-full flex-wrap justify-between py-3 text-sm font-bold text-gray-700 sm:text-left sm:text-xl"
					>
						<p>Java</p>
						<p>Swing</p>
						<p>API</p>
					</div>

          <div class="flex justify-between">
					<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
						<a href="/radioInfo"> Läs mer </a>
					</p>
					<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
          <a href="/RadioInfo.jar" download> Ladda ned körbar JAR-fil </a>
					</p>
          </div>
				</div>
			</div>
		</div>


		<div class=" h-screen snap-center sm:pt-10" id="skrivert">
			<h1 class="pb-16 text-center text-lg font-bold tracking-tight">Mina projekt</h1>
			<div class="container items-center justify-center sm:grid sm:grid-cols-2">
				<div class="sm:order-2" id="skrivert right">
					<Carousel.Root
						opts={{
							align: 'start',
							loop: true
						}}
					>
						<Carousel.Content class="mx-auto">
							<Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">1 / 3</p>
								<button on:click={() => enlargeImage('skrivert_gif')}>
									<img
										src={skrivert_gif}
										alt="skrivert gif som jag har gjort"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>
								<p class="text-md py-3 text-center font-semibold leading-none">
									En kampanj-gif gjord för skrivert
								</p>
							</Carousel.Item>
							<Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">2 / 3</p>
								<button on:click={() => enlargeImage('skrivert_skriva')}>
									<img
										src={skrivert_skriva}
										alt="skrivert skriva"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>

								<p class="text-md py-3 text-center font-semibold leading-none">
									Bild från skriverts skriva-vy. Detta är huvudvyn i programmet.
								</p>
							</Carousel.Item>
							<Carousel.Item>
								<p class="text-md py-3 text-center font-semibold leading-none">3 / 3</p>
								<button on:click={() => enlargeImage('skrivert_settings')}>
									<img
										src={skrivert_settings}
										alt="skrivert inställningar"
										class="mx-auto object-cover sm:w-5/6"
									/>
								</button>
								<p class="text-md py-3 text-center font-semibold leading-none">
									Bild från skriverts inställningsvy
								</p>
							</Carousel.Item>
						</Carousel.Content>
						{#if $isDesktop}
							<Carousel.Previous />
							<Carousel.Next />
						{/if}
					</Carousel.Root>
				</div>

				<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="skrivert left">
					<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
						skrivert
					</h1>

					<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
						Projekt för att skapa GUI till ett textproduktionsprogram
					</h3>

					<div
						class="mx-auto flex w-full flex-wrap justify-between py-3 text-sm font-bold text-gray-700 sm:text-left sm:text-xl"
					>
						<p>Figma</p>
						<p>Svelte</p>
						<p>ShadCN</p>
						<p>Tailwind</p>
						<p>Design-Build-Test</p>
					</div>

					<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
						<a href="/skrivert"> Läs mer </a>
					</p>
				</div>
			</div>
		</div>

		<div
			class="container grid h-screen snap-center items-center py-16 sm:grid-cols-2 sm:py-0"
			id="jointfly"
		>
			<div class="sm:order-2" id="jointfly right">
				<Carousel.Root
					opts={{
						align: 'start',
						loop: true
					}}
				>
					<Carousel.Content class="mx-auto">
						<Carousel.Item>
							<p class="text-md py-3 text-center font-semibold leading-none">1 / 2</p>
							<button on:click={() => enlargeImage('jointfly_start')}>
								<img
									src={jointfly_start}
									alt="jointfly startskärm"
									class="mx-auto object-cover sm:w-5/6"
								/>
							</button>
							<p class="text-md py-3 text-center font-semibold leading-none">
								jointflys startskärm
							</p>
						</Carousel.Item>
						<Carousel.Item>
							<p class="text-md py-3 text-center font-semibold leading-none">2 / 2</p>
							<button on:click={() => enlargeImage('jointfly_play')}>
								<img
									src={jointfly_play}
									alt="jointfly körs"
									class="mx-auto object-cover sm:w-5/6"
								/>
							</button>

							<p class="text-md py-3 text-center font-semibold leading-none">
								Bild på när jointfly körs
							</p>
						</Carousel.Item>
					</Carousel.Content>
					{#if $isDesktop}
						<Carousel.Previous />
						<Carousel.Next />
					{/if}
				</Carousel.Root>
			</div>

			<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="jointfly left">
				<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
					jointfly!
				</h1>

				<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
					En prototyp av en app gjord för att styra flera drönare samtidigt från en mobil enhet.
				</h3>

				<div
					class="mx-auto flex w-3/4 flex-wrap justify-between py-3 text-sm font-bold text-gray-700 sm:w-full sm:text-left sm:text-xl"
				>
					<p>Figma</p>
					<p>Användarstudier</p>
					<p>Prototyping</p>
				</div>

				<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
					<a href="/jointfly"> Läs mer </a>
				</p>
			</div>
		</div>

		<div
			class="container grid h-screen snap-center items-center py-16 sm:grid-cols-2 sm:py-0"
			id="grafikmotor"
		>
			<div class="sm:order-2" id="grafikmotor right">
				<Carousel.Root
					opts={{
						align: 'start',
						loop: true
					}}
				>
					<Carousel.Content class="mx-auto">
						<Carousel.Item>
							<p class="text-md py-3 text-center font-semibold leading-none">1 / 3</p>
							<button on:click={() => enlargeImage('three_d_studio_one')}>
								<img
									src={three_d_studio_one}
									alt="3D studio bild 1"
									class="mx-auto object-cover sm:w-5/6"
								/>
							</button>

							<p class="text-md py-3 text-center font-semibold leading-none">3D Studio</p>
						</Carousel.Item>
						<Carousel.Item>
							<p class="text-md py-3 text-center font-semibold leading-none">2 / 3</p>
							<button on:click={() => enlargeImage('three_d_parallel')}>
								<img
									src={three_d_parallel}
									alt="Parallel Projektion"
									class="mx-auto object-cover sm:w-5/6"
								/>
							</button>

							<p class="text-md py-3 text-center font-semibold leading-none">Parallel Projection</p>
						</Carousel.Item>
						<Carousel.Item>
							<p class="text-md py-3 text-center font-semibold leading-none">3 / 3</p>
							<button on:click={() => enlargeImage('three_d_oblique')}>
								<img
									src={three_d_oblique}
									alt="Oblik Projektion"
									class="mx-auto object-cover sm:w-5/6"
								/>
							</button>
							<p class="text-md py-3 text-center font-semibold leading-none">Oblique Projection</p>
						</Carousel.Item>
					</Carousel.Content>
					{#if $isDesktop}
						<Carousel.Previous />
						<Carousel.Next />
					{/if}
				</Carousel.Root>
			</div>

			<div class="px-3 sm:container sm:w-3/5 sm:px-0" id="grafikmotor left">
				<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
					3D Studio
				</h1>

				<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
					Simpel grafikmotor skriven i C++ med hjälp av OpenGL, GLM och tinyOBJloader
				</h3>

				<div
					class="mx-auto flex w-3/4 justify-between py-3 text-sm font-bold text-gray-700 sm:w-full sm:text-left sm:text-xl"
				>
					<p>C++</p>
					<p>OpenGL</p>
					<p>Datorgrafik</p>
				</div>

        <div class="flex justify-between">
				<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
					<a href="/3dstudio"> Läs mer </a>
				</p>
				<p class="py-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
					<a href="https://github.com/jfkgustav/3dstudio"> GitHub-repo </a>
				</p>
        </div>
			</div>
		</div>

		<div
			class="container grid h-screen snap-center items-center py-16 sm:grid-cols-2 sm:py-0"
			id="recharge"
		>
			<div class="sm:order-2" id="recharge right">
				<img src={recharge} alt="recharge" class="mx-auto w-full sm:w-5/6" />
				<p class="py-3 text-center text-xl font-semibold leading-none">RECHARGE</p>
			</div>

			<div class=" px-3 sm:container sm:w-3/5 sm:px-0" id="recharge left">
				<h1 class="text-center text-4xl font-extrabold tracking-tight sm:text-left lg:text-5xl">
					RECHARGE
				</h1>

				<h3 class="text-md py-3 text-center font-semibold sm:text-left sm:text-3xl">
					En prototyp av en app gjord för att smidigt hitta och boka laddstationer för elbilar
				</h3>

				<div
					class="mx-auto flex w-full flex-wrap justify-between py-3 text-sm font-bold text-gray-700 sm:text-left sm:text-xl"
				>
					<p>Figma</p>
					<p>Användarstudier</p>
					<p>Wireframes</p>
					<p>Prototyping</p>
				</div>

				<p class="pt-3 text-center text-sm font-semibold text-blue-500 sm:text-left sm:text-xl">
					<a href="/recharge"> Läs mer </a>
				</p>
			</div>
		</div>
	</div>

	<div class="fixed inset-0 hidden h-screen" id="large_div">
		<div class="  h-dvh bg-black/50 backdrop-blur-sm">
			<div class="h-screen">
				<button
					id="exit_button"
					on:click={() => enlargeImage('recharge')}
					class="flex h-full w-screen -translate-y-32 scale-50 items-center justify-center py-12 transition-all duration-200 focus:translate-x-0 focus:translate-y-0 focus:scale-100 sm:translate-x-96 sm:translate-y-0"
				>
					<img src={large_img_src} alt="stor bild" class="z-40 h-full object-contain" />
				</button>
			</div>
		</div>
	</div>
</div>
