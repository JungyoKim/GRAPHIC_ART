<script>
    export let show = true;
    export let title = '';
    export let content = '';

    function closeModal() {
        show = false;
    }
</script>

{#if show}
<div class="fixed z-10 w-full inset-0 overflow-y-auto p-[50px]" role="dialog">
    <div class="flex items-center justify-center min-h-screen">
        <div class="bg-white p-6 rounded shadow-lg text-center">
            <h2 class="text-[80px] mb-4 font-bold">{title}</h2>
            <p class="text-[40px]">{content}</p>
            <div class="mt-4">
                <button class="bg-gray-700 text-white px-4 py-2 rounded" on:click={closeModal}>닫기</button>
            </div>
        </div>
    </div>
</div>
{/if}
