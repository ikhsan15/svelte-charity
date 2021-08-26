<script>
	import router from "page";
	import Home from "./pages/Home.svelte";
	import About from "./pages/About.svelte";
	import Contact from "./pages/Contact.svelte";
	import Donation from "./pages/Donation.svelte";
	import NotFound from "./pages/NotFound.svelte";
	import Success from "./pages/Success.svelte";

	let page, params;

	// mendefinisikan router yg digunakan
	router("/", () => (page = Home));
	router("/about", () => (page = About));
	router("/contact", () => (page = Contact));
	router("/success", () => (page = Success));
	router(
		"/donation/:id",
		(ctx, next) => {
			params = ctx.params;
			next();
		},
		() => (page = Donation)
	);

	// pastikan halaman NotFound berada di paling bawah
	// start -- router NotFound
	router("/*", () => (page = NotFound));
	// finish -- router NotFound

	router.start();
</script>

<!-- mengubah komponen svelte untuk merender halaman dimana kita berada saat ini
  -->
<svelte:component this={page} {params} />
