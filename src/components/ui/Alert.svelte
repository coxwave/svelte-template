<script lang="ts">
  import clsx from 'clsx';
  import { ExclamationIcon } from 'heroicons-svelte/outline';

  import type { ApiErrorJson } from '$utils/errors';

  export let error: ApiErrorJson;
</script>

<div class={clsx($$props.class, 'rounded-md bg-yellow-50 p-4')}>
  <div class="flex">
    <div class="flex-shrink-0">
      <ExclamationIcon class="h-5 w-5 text-yellow-400" />
    </div>
    <div class="ml-3">
      <h3 class="text-sm font-medium text-yellow-800">[{error.code}] {error.name}</h3>
      <div class="mt-2 text-sm text-yellow-700">
        <p>
          {error.message}
        </p>
      </div>
    </div>
  </div>
</div>
