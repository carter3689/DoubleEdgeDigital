<script>
    import '../app.css';
    import HeaderAgencyError from  '../components/page_not_found_header.svelte';
    import HeaderAgencyConstruction from  '../components/coming_soon_header.svelte';
    import Footer from '../components/footer.svelte';
    export let message;
    let status
</script>

<script context="module">
    /** @type {import('@sveltejs/kit').Load} */
    export function load({ error, status }) {
      return {
        props: {
          message: error.message,
          status
        }
      };
    }
  </script>

{#if status == 404}
<HeaderAgencyError />
<slot />
<Footer />

{:else}
<HeaderAgencyConstruction />
<slot />
<Footer />

{/if}