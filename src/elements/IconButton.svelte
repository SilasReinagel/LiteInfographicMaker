<script>
  export let name, icon, onClick, isMobileHidden = false, small = false;

	const width = small ? '24px' : '36px';
	const height = width; 
</script>

<button on:click={onClick} class={isMobileHidden ? "mobile-hidden" : ""}>
  <div class={"icon tooltip" + (small ? " small" : "")}>
    <img src={icon} alt={name} width={width} height={height}/>
    <div class="tooltiptext">{name}</div>
  </div>
</button>

<style>
	button {
		border: 0px;
		padding: 0.4em;
		background-color: rgba(1,1,1,0);
	}

	button:hover {
		background-color: var(--button-hover-color);
		border-radius: 12px;
	}

	.icon {
		width: 36px;
		height: 36px;
  }

	.small {
		width: 24px;
		height: 24px;
	}

  @media (max-wdith: 640px) {
		.mobile-hidden {
			display: none;
		}
	}
</style>