<script lang="ts">
  let className: string = "";
  export let primary = false;
  export let type: "submit" | "reset" | "button" | undefined | null = "button";
  export { className as class };

  let variant = primary
    ? "bg-primary-400 dark:border text-black hover:bg-primary-500 focus:bg-primary-600"
    : "shadow-sm bg-gray-50 hover:bg-white hover:shadow-md border border-gray-300";

  let classes = className + " " + variant;
</script>

<button
  on:click
  {type}
  class="{classes} rounded-md px-3 py-1 font-medium transition-colors dark:border-gray-700 dark:bg-gray-900 dark:text-white dark:hover:bg-gray-950 dark:focus:border-gray-700 dark:focus:bg-gray-800">
  <slot />
</button>
