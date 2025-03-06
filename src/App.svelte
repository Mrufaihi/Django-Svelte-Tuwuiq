<script lang="ts">
  import Button from './lib/components/ui/button/button.svelte';
  import Array from '$lib/Array.svelte';
  import Input from '$lib/components/ui/input/input.svelte';
  import Label from '$lib/components/ui/label/label.svelte';

  const companies = ['Apple', 'GOOGLE'];

  let companyInput = '';

  $: if (companies.map((c) => c.toUpperCase()).includes(companyInput.toUpperCase())) {
    console.log('Yes!', companyInput);
  } else {
    console.log('No', companyInput);
  }
</script>

<main>
  <div class="container m-5">
    <Label>Companies</Label>
    <Input type="text" bind:value={companyInput} />
  </div>
</main>
