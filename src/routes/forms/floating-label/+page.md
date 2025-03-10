---
layout: formLayout
---

<script>
  import { Htwo, ExampleDiv, GitHubSource, CompoDescription, TableProp, TableDefaultRow} from '../../utils'
  import { FloatingLabelInput, Helper, Breadcrumb, BreadcrumbItem, Badge } from '$lib'
  import { Home } from 'svelte-heros'
  import componentProps from '../../props/FloatingLabelInput.json'
   import componentProps2 from '../../props/Helper.json'
  let items = componentProps.props
  let items2 = componentProps2.props
  
  let propHeader = ['Name', 'Type', 'Default']
  let divClass='w-full relative overflow-x-auto shadow-md sm:rounded-lg py-4'
  let theadClass ='text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-white'
</script>

<Breadcrumb>
  <BreadcrumbItem href="/" icon={Home} variation="solid">Home</BreadcrumbItem>
  <BreadcrumbItem href="/forms/" rel="external">Forms</BreadcrumbItem>
  <BreadcrumbItem>Floating label</BreadcrumbItem>
</Breadcrumb>

<h1 class="text-3xl w-full dark:text-white pt-8 pb-4">Floating label</h1>

<CompoDescription>Use the floating label style for the input field elements to replicate the Material UI design system from Google and choose from multiple styles and sizes</CompoDescription>

<ExampleDiv>
<GitHubSource href="forms/FloatingLabelInput.svelte">FloatingLabel</GitHubSource>
</ExampleDiv>

The floating label style was first pioneered by Google in its infamous Material UI design system and it’s basically a label tag which floats just above the input field when it is being focused or already has content inside.

On this page you will find a three different input field styles including a standard, outlined, and filled style including validation styles and sizes coded with Tailwind CSS and supported for dark mode.

<Htwo label="Setup" />

```html
<script>
	import { FloatingLabelInput, Helper } from 'flowbite-svelte';
</script>
```

<Htwo label="Floating label examples" />

Get started with the following three styles for the floating label component and use the label tag as a visual placeholder using the peer-placeholder-shown and peer-focus utility classes from Tailwind CSS.

<ExampleDiv>
<div id="exampleWrapper" class="grid gap-6 items-end w-full md:grid-cols-3">
<FloatingLabelInput style="filled" id="floating_filled" name="floating_filled" type="text" label="Floating filled"/>
<FloatingLabelInput style="outlined" id="floating_outlined" name="floating_outlined" type="text" label="Floating outlined" />
<FloatingLabelInput id="floating_standard" name="floating_standard" type="text" label="Floating standard" />
</div>
</ExampleDiv>

```html
<script>
  import { FloatingLabelInput } from 'flowbite-svelte'
</script>

<FloatingLabelInput style="filled" id="floating_filled" name="floating_filled" type="text" label="Floating filled"/>
<FloatingLabelInput style="outlined" id="floating_outlined" name="floating_outlined" type="text" label="Floating outlined" />
<FloatingLabelInput id="floating_standard" name="floating_standard" type="text" label="Floating standard" />
```

<Htwo label="Disabled state" />

Apply the disabled attribute to the input fields to disallow the user from changing the content.

<ExampleDiv>
<div id="exampleWrapper" class="grid gap-6 items-end w-full md:grid-cols-3">
<FloatingLabelInput style="filled" id="disabled_filled" name="disabled_filled" type="text" label="Disabled filled" disabled/>
<FloatingLabelInput style="outlined" id="disabled_outlined" name="disabled_outlined" type="text" label="Disabled outlined" disabled/>
<FloatingLabelInput id="disabled_standard" name="disabled_standard" type="text" label="Disabled standard" disabled/>
</div>
</ExampleDiv>

```html
<div id="exampleWrapper" class="grid gap-6 items-end w-full md:grid-cols-3">
<FloatingLabelInput style="filled" id="disabled_filled" name="disabled_filled" type="text" label="Disabled filled" disabled/>
<FloatingLabelInput style="outlined" id="disabled_outlined" name="disabled_outlined" type="text" label="Disabled outlined" disabled/>
<FloatingLabelInput id="disabled_standard" name="disabled_standard" type="text" label="Disabled standard" disabled/>
</div>
```

<Htwo label="Validation" />

Use the following examples of input validation for the success and error messages by applying the validation text below the input field and using the green or red color classes from Tailwind CSS.

<ExampleDiv>
<!-- Success messages -->
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
  <div>
    <FloatingLabelInput color="green" style="filled" id="filled_success" aria-describedby="filled_success_help" name="filled_success" type="text" label="Filled success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="green" style="outlined" id="outlined_success" aria-describedby="outlined_success_help" name="outlined_success" type="text" label="Outlined success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="green" style="standard" id="standard_success" aria-describedby="standard_success_help" name="standard_success" type="text" label="Standard success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
</div>
<!-- Error messages -->
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
  <div>
    <FloatingLabelInput color="red" style="filled" id="filled_error" aria-describedby="filled_error_help" name="filled_error" type="text" label="Filled error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="red" style="outlined" id="outlined_error" aria-describedby="outlined_error_help" name="outlined_success" type="text" label="Outlined error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="red" style="standard" id="standard_error" aria-describedby="standard_error_help" name="standard_success" type="text" label="Standard error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
</div>
</ExampleDiv>

```html
<!-- Success messages -->
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
  <div>
    <FloatingLabelInput color="green" style="filled" id="filled_success" aria-describedby="filled_success_help" name="filled_success" type="text" label="Filled success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="green" style="outlined" id="outlined_success" aria-describedby="outlined_success_help" name="outlined_success" type="text" label="Outlined success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="green" style="standard" id="standard_success" aria-describedby="standard_success_help" name="standard_success" type="text" label="Standard success"/>
    <Helper color="green"><span class="font-medium">Well done!</span> Some success message.</Helper>
  </div>
</div>
<!-- Error messages -->
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
  <div>
    <FloatingLabelInput color="red" style="filled" id="filled_error" aria-describedby="filled_error_help" name="filled_error" type="text" label="Filled error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="red" style="outlined" id="outlined_error" aria-describedby="outlined_error_help" name="outlined_success" type="text" label="Outlined error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
  <div>
    <FloatingLabelInput color="red" style="standard" id="standard_error" aria-describedby="standard_error_help" name="standard_success" type="text" label="Standard error"/>
    <Helper color="red"><span class="font-medium">Oh, snapp!</span> Some error message.</Helper>
  </div>
</div>
```

<Htwo label="Sizes" />

Use the small and default sizes of the floating label input fields from the following example.

<ExampleDiv>
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
<FloatingLabelInput size="small" style="filled" id="small_filled" name="small_filled" type="text" label="Small filled"/>
<FloatingLabelInput size="small" style="outlined" id="small_outlined" name="small_outlined" type="text" label="Small outlined" />
<FloatingLabelInput size="small" id="small_standard" name="small_standard" type="text" label="Small standard" />
</div>
<div class="grid gap-6 items-end md:grid-cols-3">
<FloatingLabelInput style="filled" id="default_filled" name="default_filled" type="text" label="Default filled"/>
<FloatingLabelInput style="outlined" id="default_outlined" name="default_outlined" type="text" label="Default outlined" />
<FloatingLabelInput id="default_standard" name="default_standard" type="text" label="Default standard" />
</div>
</ExampleDiv>

```html
<div class="grid gap-6 items-end mb-6 md:grid-cols-3">
<FloatingLabelInput size="small" style="filled" id="small_filled" name="small_filled" type="text" label="Small filled"/>
<FloatingLabelInput size="small" style="outlined" id="small_outlined" name="small_outlined" type="text" label="Small outlined" />
<FloatingLabelInput size="small" id="small_standard" name="small_standard" type="text" label="Small standard" />
</div>
<div class="grid gap-6 items-end md:grid-cols-3">
<FloatingLabelInput style="filled" id="default_filled" name="default_filled" type="text" label="Default filled"/>
<FloatingLabelInput style="outlined" id="default_outlined" name="default_outlined" type="text" label="Default outlined" />
<FloatingLabelInput id="default_standard" name="default_standard" type="text" label="Default standard" />
</div>
```

<Htwo label="Helper text" />

Add a helper text in addition to the label if you want to show more information below the input field.

<ExampleDiv>
<FloatingLabelInput style="filled" id="floating_helper" aria-describedby="floating_helper_text" name="floating_helper" type="text" label="Floating helper"/>
<Helper>Remember, contributions to this topic should follow our <a href="/" class="text-blue-600 dark:text-blue-500 hover:underline">Community Guidelines</a>.</Helper>
</ExampleDiv>

```html
<FloatingLabelInput style="filled" id="floating_helper" aria-describedby="floating_helper_text" name="floating_helper" type="text" label="Floating helper"/>
<Helper>Remember, contributions to this topic should follow our <a href="/" class="text-blue-600 dark:text-blue-500 hover:underline">Community Guidelines</a>.</Helper>
```

<Htwo label="Props" />

The component has the following props, type, and default values. See <a href="/pages/types">types 
 page</a> for type information.

<TableProp header={propHeader} {divClass} {theadClass}>
  <TableDefaultRow {items} rowState='hover' />
</TableProp>

<h3 class='text-xl w-full dark:text-white py-4'>Helper</h3>

<TableProp header={propHeader} {divClass} {theadClass}>
<TableDefaultRow items={items2} rowState='hover' />
</TableProp>

<Htwo label="Forwarded Events" />

<div class="flex flex-wrap gap-2">
<Badge large={true}>on:blur</Badge>
<Badge large={true}>on:change</Badge>
<Badge large={true}>on:click</Badge>
<Badge large={true}>on:focus</Badge>
<Badge large={true}>on:keydown</Badge>
<Badge large={true}>on:keypress</Badge>
<Badge large={true}>on:keyup</Badge>
<Badge large={true}>on:mouseenter</Badge>
<Badge large={true}>on:mouseleave</Badge>
<Badge large={true}>on:mouseover</Badge>
<Badge large={true}>on:paste</Badge>
</div>
