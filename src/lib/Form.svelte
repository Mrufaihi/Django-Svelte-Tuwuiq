<script lang="ts">
  import { Input } from './components/ui/input/index';
  import { CardHeader, CardContent, CardDescription, Card } from './components/ui/card/index';
  import { Label } from './components/ui/label/index';
  import {
    Select,
    SelectTrigger,
    SelectValue,
    SelectContent,
    SelectItem,
    SelectGroup,
  } from '$lib/components/ui/select/index.js';
  import { Button } from '$lib/components/ui/button/index';
  import { Checkbox } from '$lib/components/ui/checkbox/index';
  import { RadioGroup, RadioGroupItem } from '$lib/components/ui/radio-group/index';

  // You'll need to create a form instance with superForm
  // This is just a placeholder - replace with your actual form schema
</script>

<main>
  <div class="container mt-5" dir="rtl">
    <Card class="gap-5 bg-gray-50">
      <CardHeader>
        <h1 class="text-4xl font-bold">تسجيل الموظف</h1>
      </CardHeader>
      <CardContent class="">
        <form class="container grid gap-5 rtl">
          <!--  -->
          <div class="grid grid-cols-3 gap-3">
            <div class="">
              <Label>رقم الموظف</Label>
              <Input type="email" />
            </div>
            <div class="">
              <Label>اسم الموظف</Label>
              <Input type="text" />
            </div>
            <div class="">
              <Label>عنوان الموظف</Label>
              <Input type="text" />
            </div>
          </div>
          <!--  -->
          <div class="grid grid-cols-2 gap-3 mt-5">
            <div class="">
              <Select>
                <SelectTrigger>
                  <SelectValue placeholder="اختر المنطقة" />
                </SelectTrigger>
                <SelectContent>
                  <SelectItem value="makkah">مكه</SelectItem>
                  <SelectItem value="riyadh">الرياض</SelectItem>
                </SelectContent>
              </Select>
            </div>
            <div class="">
              <Select>
                <SelectTrigger>
                  <SelectValue placeholder="اختر المدينة" />
                </SelectTrigger>
                <SelectContent>
                  <SelectItem value="jeddah">جدة</SelectItem>
                  <SelectItem value="makkah">مكه</SelectItem>
                </SelectContent>
              </Select>
            </div>
          </div>
          <!--  -->
          <div class="grid grid-cols-2 gap-3 mt-3">
            <div class="flex">
              <Label for="checkbox-1" class="mx-2">على راس العمل</Label>
              <Checkbox id="checkbox-1" />
            </div>

            <!-- default value -->

            <RadioGroup value="option-1" class="">
              <div class="flex">
                <Label for="radio-1" class="mx-2">معتمد</Label>
                <RadioGroupItem id="radio-1" value="option-1" />
              </div>
              <div class="flex">
                <Label for="radio-2" class="mx-2">تحت التدريب</Label>
                <RadioGroupItem id="radio-2" value="option-2" />
              </div>
            </RadioGroup>
          </div>

          <!--  -->
          <div class="grid mt-3">
            <Button class="justify-center" size="lg">ارسال</Button>
          </div>
        </form>
      </CardContent>
    </Card>
  </div>
</main>

<style>
  .html {
    font-family: 'Rubik', sans-serif;
  }
</style>
