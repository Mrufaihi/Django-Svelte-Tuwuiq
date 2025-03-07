<script lang="ts">
  import Button from './lib/components/ui/button/button.svelte';
  import Array from '$lib/Array.svelte';
  import Input from '$lib/components/ui/input/input.svelte';
  import Label from '$lib/components/ui/label/label.svelte';
  import { Card, CardContent, CardHeader, CardTitle } from '$lib/components/ui/card/index';
  import {
    TableBody,
    TableHead,
    TableRow,
    TableCell,
    TableHeader,
    Table,
  } from '$lib/components/ui/table/index';
  import { ModeWatcher } from 'mode-watcher';
  // import { SaudiRiyal } from '/saudi-riyal.svg';

  const companies = ['Apple', 'GOOGLE'];

  let companyInput = '';

  $: if (companies.map((c) => c.toUpperCase()).includes(companyInput.toUpperCase())) {
    console.log('Yes!', companyInput);
  } else {
    console.log('No', companyInput);
  }
</script>

<main class="container min-h-screen" dir="rtl">
  <!-- dark mode -->
  <ModeWatcher />
  <div class="flex flex-col gap-10">
    <!-- header -->
    <header class="flex items-center justify-between border-b-2 p-3" dir="ltr">
      <img src="./car-logo.png" class="w-[100px] rounded-full" alt="" />
      <div class="text-2xl">الشركه العالميه</div>
      <div class="">
        <a href="mailto:Malrufaihi@gmail.com">Malrufaihi@gmail.com</a>
        <span>|</span>
        <a href="tel: 966549584881">0540584882</a>
      </div>
    </header>

    <!-- CARD INFO -->
    <section class="container">
      <Table class="text-center">
        <TableHeader>
          <TableRow class="">
            <TableCell>رقم السياره</TableCell>
            <TableCell>اسم السياره</TableCell>
            <TableCell>اللون</TableCell>
            <TableCell>السعر</TableCell>
          </TableRow>
        </TableHeader>
        <TableBody>
          <TableRow>
            <TableCell>1</TableCell>
            <TableCell>كورولا</TableCell>
            <TableCell>ابيض</TableCell>
            <TableCell class="flex justify-center gap-2">
              68000
              <img src="./saudi-riyal.svg" class="w-[15px]" alt="" />
            </TableCell>
          </TableRow>
          <TableRow>
            <TableCell>2</TableCell>
            <TableCell>كامري</TableCell>
            <TableCell>ابيض</TableCell>
            <TableCell class="flex justify-center gap-2">
              100000
              <img src="./saudi-riyal.svg" class="w-[15px]" alt="" />
            </TableCell>
          </TableRow>
        </TableBody>
      </Table>
    </section>
    <!-- RATING -->

    <section class="container">
      <Card class="flex  justify-between">
        <CardContent class="flex flex-col items-center justify-between">
          <h2 class="text-3xl">التقييم: ٩.٥</h2>
          <h2 class="text-3xl">المشاهدات: ١٠٠٠</h2>
          <h2 class="text-3xl">الموقع: الرياض</h2>
        </CardContent>
        <CardContent class=" flex flex-col items-center justify-between">
          <h2 class="text-3xl">المواصفات</h2>
          <h2 class="text-3xl">الموديل: كامري ٢٠٢٤</h2>
          <h2 class="text-3xl">المحرك: ٣.٥ في ٦ سلندر</h2>
          <h2 class="text-3xl">اللون: ابيض</h2>
          <h2 class="text-3xl">الفير: اوتاماتيك ٨ سرعات</h2>
        </CardContent>
        <CardContent>
          <img
            src="./Toyota Camry 70 3_5 V6.jpeg"
            class="max-w-[150px] rounded-md object-contain"
            alt=""
          />
        </CardContent>
      </Card>
    </section>
    <!-- todo: footer -->
    <footer>
      <div></div>
    </footer>
  </div>
</main>
