<script>
  import Icon from "./Icon.svelte";
  const list = [
    { name: "Главная", icon: "home" },
    { name: "Поиск", icon: "svelte" },
  ];
</script>

<div class="sidebar-left-menu">
  {#each list as item}
    <div class="sidebar-left-menu__item">
      <span><Icon name={item.icon} /></span>
      <span>{item.name}</span>
    </div>
  {/each}
</div>

<style>
  .sidebar-left-menu__item {
    display: flex;
    gap: 20px;
    align-items: center;
  }
  .sidebar-left-menu {
    display: flex;
    flex-direction: column;
  }
</style>
