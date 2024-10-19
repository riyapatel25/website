<script>
	import { collection, addDoc } from 'firebase/firestore';
	import { db } from '../../lib/firebase';

	let email = '';
	let loading = false;
	let done = false;

	const subscribe = async () => {
		// Implement the function to handle the subscription
		console.log(email);
		loading = true;
		const docRef = await addDoc(collection(db, 'subscriptions'), {
			createdAt: new Date(),
			email: email
		});
		loading = false;
		done = true;
		email = '';
	};
</script>

<svelte:head>
	<title>John Qian's blog</title>
	<meta
		name="description"
		content="The blog of John Qian. I'm tacking my name onto my site metadata to bump my SEO for my name."
	/>
</svelte:head>
<h1>Welcome!</h1>
<p>
	My name is Riya Patel. I'm studying software engineering at UWaterloo and have fun working on projects that add value to the world. Currently working on firmware on <a
		href="https://www.uworbital.com/"
		target="_blank">Orbital</a
	> and 
	<a
		href="https://www.waterloorocketry.com/"
		target="_blank">Rocketry</a
	>.

</p>

<p>
	Feel free to reach out to me at <a
		href="mailto:riya.patel1@uwaterloo.ca">riya.patel1@uwaterloo.ca</a
	>
</p>
<div class="flex gap-2 items-center mt-8">
	<a target="_blank" rel="noreferrer" href="https://x.com/riyapee">
		<img alt="twitter profile" src="twitter.svg" class="h-4 hover:brightness-110" />
	</a>
	<a target="_blank" rel="noreferrer" href="https://github.com/riyapatel25">
		<img alt="github profile" src="github.svg" class="h-5 rounded-full hover:opacity-90" />
	</a>
</div>

{#if done}
	<p class="mt-2 text-sm text-gray-500">Thank you!</p>
{/if}
