<script>
	import { signIn, signOut } from '@auth/sveltekit/client';
	import { page } from '$app/stores';
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
					on:click={() => signIn('github')}
					class="btn variant-ringed-primary inline-flex items-center justify-center w-full px-4 py-2 rounded-md shadow-sm text-sm leading-5 font-medium focus:outline-none  focus:shadow-outline-blue  transition duration-150 ease-in-out"
				>
					<svg class="h-5 w-5 mr-2" viewBox="0 0 24 24" fill="currentColor">
						<path
							fill-rule="evenodd"
							d="M12 0C5.373 0 0 5.373 0 12c0 5.275 3.438 9.732 8.205 11.317.6.111.82-.258.82-.576 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.562-4.042-1.562-.546-1.387-1.333-1.757-1.333-1.757-1.09-.745.083-.729.083-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.834 2.809 1.304 3.494.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.385 1.235-3.222-.135-.303-.535-1.524.104-3.176 0 0 1.007-.322 3.3 1.23a11.534 11.534 0 0 1 3-.4c1.02 0 2.04.136 3 .4 2.292-1.552 3.3-1.23 3.3-1.23.64 1.652.24 2.873.12 3.176.765.837 1.23 1.912 1.23 3.222 0 4.61-2.805 5.627-5.475 5.917.42.36.81 1.096.81 2.215 0 1.597-.015 2.884-.015 3.27 0 .318.215.694.825.576C20.565 21.73 24 17.274 24 12c0-6.627-5.373-12-12-12z"
						/>
					</svg>
					Sign in with GitHub
				</button>
			</div>
		</div>
	</div>
</div>
