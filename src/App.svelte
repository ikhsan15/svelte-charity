<script>
	import router from "page";
	import Home from "./pages/Home.svelte";
	import About from "./pages/About.svelte";
	import Contact from "./pages/Contact.svelte";

	let page;

	// mendefinisikan router yg digunakan
	router("/", () => (page = Home));
	router("/about", () => (page = About));
	router("/contact", () => (page = Contact));

	router.start();
</script>

<!-- mengubah komponen svelte untuk merender halaman dimana kita berada saat ini
  -->
<svelte:component this={page} />
