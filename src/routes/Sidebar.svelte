<script>
	import SidebarItem from './SidebarItem.svelte';
</script>

<div class="w-60 shrink-0 h-full">
	<div class="list-none flex flex-col pt-10 sticky top-0">
		<SidebarItem to="/">Home</SidebarItem>
		<SidebarItem to="/box">Lock Box</SidebarItem>
		<SidebarItem to="/remy">Ratatouille</SidebarItem>
		<SidebarItem to="/drone">Heat Tile Crack Detection Drone</SidebarItem>
		<SidebarItem to="/internships">Internships</SidebarItem>
		<SidebarItem to="/moon">Why Engineering on the Moon is Hard</SidebarItem>
	</div>
</div>
