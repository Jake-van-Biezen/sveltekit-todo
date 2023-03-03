<script lang="ts">
	import { signIn } from '@auth/sveltekit/client';
	let loading = false;

	const handleClick = () => {
		loading = true;
		signIn('github');
	};
</script>

<div class="min-h-screen flex items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
	<div class="max-w-md w-full">
		<div>
			<h2 class="mt-6 text-center text-3xl leading-9 font-extrabold">
				Sign in to start your todo journey
			</h2>
		</div>
		<div class="mt-8">
			<div>
				<button
					on:click={() => handleClick()}
					class="btn variant-ringed-primary inline-flex items-center justify-center w-full px-4 py-2 rounded-md shadow-sm text-sm leading-5 font-medium focus:outline-none  focus:shadow-outline-blue  transition duration-150 ease-in-out"
				>
					{#if loading}
						Signing in...&nbsp;&nbsp;
						<div role="status">
							<svg
								aria-hidden="true"
								class="inline w-8 h-8 mr-2 text-gray-200 animate-spin dark:text-gray-600 fill-red-600"
								viewBox="0 0 100 101"
								fill="none"
								xmlns="http://www.w3.org/2000/svg"
							>
								<path
									d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
									fill="currentColor"
								/>
								<path
									d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
									fill="currentFill"
								/>
							</svg>
							<span class="sr-only">Loading...</span>
						</div>
					{:else}
						<svg class="h-5 w-5 mr-2" viewBox="0 0 24 24" fill="currentColor">
							<path
								fill-rule="evenodd"
								d="M12 0C5.373 0 0 5.373 0 12c0 5.275 3.438 9.732 8.205 11.317.6.111.82-.258.82-.576 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.562-4.042-1.562-.546-1.387-1.333-1.757-1.333-1.757-1.09-.745.083-.729.083-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.834 2.809 1.304 3.494.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.385 1.235-3.222-.135-.303-.535-1.524.104-3.176 0 0 1.007-.322 3.3 1.23a11.534 11.534 0 0 1 3-.4c1.02 0 2.04.136 3 .4 2.292-1.552 3.3-1.23 3.3-1.23.64 1.652.24 2.873.12 3.176.765.837 1.23 1.912 1.23 3.222 0 4.61-2.805 5.627-5.475 5.917.42.36.81 1.096.81 2.215 0 1.597-.015 2.884-.015 3.27 0 .318.215.694.825.576C20.565 21.73 24 17.274 24 12c0-6.627-5.373-12-12-12z"
							/>
						</svg>
						Sign in with GitHub
					{/if}
				</button>
			</div>
		</div>
	</div>
</div>
