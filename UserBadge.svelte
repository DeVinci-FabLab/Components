<script>
	export let user = {
		name: 'Morgan',
		email: 'morgan@devinci.fr',
		avatar: 'https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/michael-gough.png'
	};
</script>

<button
	type="button"
	class="flex mx-3 text-sm bg-gray-800 rounded-full md:mr-0 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600"
	id="user-menu-button"
	aria-expanded="false"
	data-dropdown-toggle="dropdown"
>
	<span class="sr-only">Open user menu</span>
	<img class="w-8 h-8 rounded-full" src={user.avatar} alt="user photo" />
</button>
<!-- Dropdown menu -->
<div
	class="z-50 hidden w-56 my-4 text-base list-none bg-white divide-y divide-gray-100 rounded shadow dark:bg-gray-700 dark:divide-gray-600 rounded-xl"
	id="dropdown"
>
	<div class="px-4 py-3">
		<span class="block text-sm font-semibold text-gray-900 dark:text-white">{user.name}</span>
		<span class="block text-sm text-gray-900 truncate dark:text-white">{user.email}</span>
	</div>
	<ul class="py-1 text-gray-700 dark:text-gray-300" aria-labelledby="dropdown">
		<li>
			<a
				href="#"
				class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
				>Profil</a
			>
		</li>
		<li>
			<a
				href="#"
				class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
				>Paramètres</a
			>
		</li>
	</ul>
	<ul class="py-1 text-gray-700 dark:text-gray-300" aria-labelledby="dropdown">
		<li>
			<a
				href="#"
				class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
				on:click={() => console.log("sign out")}>Déconnexion</a
			>
		</li>
	</ul>
</div>

<style></style>
