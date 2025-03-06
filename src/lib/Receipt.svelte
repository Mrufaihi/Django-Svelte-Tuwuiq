<script lang="ts">
  import { Button } from '$lib/components/ui/button/index.js';
  import * as Card from '$lib/components/ui/card/index.js';
</script>

<Card.Root class="relative w-[350px] min-h-[500px] border-b-0 shadow-none ml-20">
  <Card.Header class="flex flex-col justify-center items-center ">
    <Card.Title>Receipt</Card.Title>
    <!-- <Card.Description>Cosco</Card.Description> -->
    <!-- <img
          src="/src/assets/contoso-receipt.png"
          class="w-[150px] object-contain rounded-lg"
          alt=""
        /> -->
  </Card.Header>
  <Card.Content>
    <form>
      <div class="grid w-full items-center gap-4">
        <div class="flex justify-between">
          <span>Name</span>
          <span>Mohammed</span>
        </div>
        <div class="flex justify-between">
          <span>Category</span>
          <span>Meal</span>
        </div>
        <div class="flex justify-between">
          <span>Item</span>
          <span>Ice cream</span>
        </div>
        <div class="flex justify-between">
          <span>Total</span>
          <span>95 Sar</span>
        </div>
      </div>
    </form>
  </Card.Content>
  <Card.Footer class="flex gap-3 w-full absolute bottom-3 ">
    <Button class="w-full" variant="outline">Cancel</Button>
    <Button class="w-full">Create</Button>
  </Card.Footer>
  <!-- Improved SVG zig-zag positioned at bottom with proper width -->
  <div class="absolute bottom-0 left-0 w-full flex justify-center">
    <svg height="12" width="100%" class="mt-2 mb-2 stroke-black">
      <path
        d="M0,0 L10,10 L20,0 L30,10 L40,0 L50,10 L60,0 L70,10 L80,0 L90,10 L100,0 L110,10 L120,0 L130,10 L140,0 L150,10 L160,0 L170,10 L180,0 L190,10 L200,0 L210,10 L220,0 L230,10 L240,0 L250,10 L260,0 L270,10 L280,0 L290,10 L300,0 L310,10 L320,0 L330,10 L340,0 L350,10"
        fill="none"
        stroke-width="1.5"
        vector-effect="non-scaling-stroke"
      />
    </svg>
  </div>
</Card.Root>

<style>
  /* Much simpler zig-zag that actually works */
  .receipt-bottom {
    height: 10px;
    width: 100%;
    background-image:
      linear-gradient(135deg, transparent 50%, #e5e7eb 50%),
      linear-gradient(225deg, transparent 50%, #e5e7eb 50%);
    background-position: top left;
    background-size: 15px 15px;
    background-repeat: repeat-x;
    position: relative;
  }
</style>
