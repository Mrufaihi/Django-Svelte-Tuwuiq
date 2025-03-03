<script lang="ts">
  import Button from './lib/components/ui/button/button.svelte';
  import * as Card from '$lib/components/ui/card/index';
</script>

<main>
  <Button class="m-3">Click pls</Button>

  <Card.Root class="justify-center items-center flex flex-col m-10 ">
    <Card.Header>
      <Card.Title>Title</Card.Title>
      <Card.Description>Descript</Card.Description>
    </Card.Header>
    <Card.Content>
      <p>Card content</p>
    </Card.Content>
    <Card.Footer>
      <p>Card footer</p>
    </Card.Footer>
  </Card.Root>
</main>
