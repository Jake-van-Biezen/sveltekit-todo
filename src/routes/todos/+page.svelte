<script>
	import { signOut } from '@auth/sveltekit/client';
</script>

<p>Hello todos</p>

<p>
	<button on:click={() => signOut('github')}>Sign out</button>
</p>
