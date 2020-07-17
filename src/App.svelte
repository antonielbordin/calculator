<script>
  export let total = 0;
	let p = 0;
	let i = 0;
	let n = 0;

	function calculateJuros () {
		total = p * i * n;
	}	
</script>

<main id="main">	
	<header class="header"><h1>Calculadora de juros simples</h1></header>
	<section class="calculator"> 
		<section class="content-pie">								
			<div class="pie-slice top-left">
				<div class="pie-one-header"> <span>P</span> </div>
				<input type="text" class="pie pie-one" bind:value={p}/>
			</div>
			<div class="pie-slice top-right">
				<div class="pie-two-header"> <span>N</span> </div>
				<input type="text" class="pie pie-two" bind:value={n}/> 
			</div>
			<div class="pie-slice bottom-left">				
				<input type="text" class="pie pie-three" bind:value={i}/>
				<div class="pie-three-header"> <span>I</span> </div>
			</div>
			<div class="pie-slice bottom-right">				
				<div class="pie pie-four"> {total} </div>
				<div class="pie-four-header"> <span>J</span> </div>				
			</div>			
		</section> 
	</section>
	<section class="action">
		<input type="button" name="calculate" value="CALCULAR" class="btn-calculate" on:click={calculateJuros} />
	</section>
	<section class="legend">
		<p><b>Legenda:</b></p>
		<p>Fórmula para o cálculo do juros simples: <b>j = P * i * n</b></p>
		<p><b>P</b> &nbsp;valor presente - principal (capital) <br> <b>i</b>&nbsp;&nbsp; taxa de juros <br> <b>n</b> &nbsp;número de períodos<br> <b>j</b>&nbsp;&nbsp; resultado do cálculo</p>
	</section>
</main>

<style>	
	#main {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}
	#main .header {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 80%;
		height: 10%;
		margin-bottom: 25px;
	}	
	#main .header h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 100; 
	}
	#main .calculator {
		width: 40%;
		height: 50%;
		padding: 10px;
	}
	#main .calculator .content-pie {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%; 
		border-radius: 50%;
		background: #ff3e00;
	}
	#main .calculator .content-pie .pie-slice {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 50%;
		height: 50%;
		color: #f2f2f2;
	}
	#main .calculator .content-pie .pie-slice .pie-one-header {
		width: 100%;
		height: 20%;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em;
	}
	#main .calculator .content-pie .pie-slice .pie-two-header {
		width: 100%;
		height: 20%;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em; 
		text-align: right;
	}
	#main .calculator .content-pie .pie-slice .pie-three-header {
		width: 100%;
		height: 20%;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em;
	}
	#main .calculator .content-pie .pie-slice .pie-four-header {
		width: 100%;
		height: 20%;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2em; 
		text-align: right;
	}
	#main .calculator .content-pie .pie-slice .pie {
		display: flex; 
		flex-direction: column;
		align-items: center;
		justify-content: center;		 
		background: transparent; 
		border: none; 
		outline: none;
		color: #f2f2f2;
	}
	#main .calculator .content-pie .pie-slice .pie-one {		
		width: 70%;
		height: 80%;
		font-size: 2em; 
		text-align: center;  
	}
	#main .calculator .content-pie .pie-slice .pie-two {
		width: 70%;
		height: 80%;
		font-size: 2em; 
		text-align: center;  
	}
	#main .calculator .content-pie .pie-slice .pie-three {
		width: 70%;
		height: 80%;
		font-size: 2em;
		text-align: center;
	}
	#main .calculator .content-pie .pie-slice .pie-four {
		width: 70%;
		height: 80%;
		font-size: 2em; 	
	}
	#main .action {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 70%;
		height: 10%;
		padding: 10px; 
		margin-top: 25px;
	}
	#main .action .btn-calculate {
		padding: 15px 18px;
		cursor: pointer;
		border: 1px solid #ff3e00;
		border-radius: 4px;
		background: transparent !important; 
		color: #ff3e00;
	}
	#main .action .btn-calculate:hover {
		background: #ff3e00 !important;
		color: #f2f2f2;
	}
	.top-left {
		border-top-left-radius: 85%; 
		background: #FF9F41;
	}
	.top-right {
		border-top-right-radius: 85%; 
		background: #F45F3E;
	}
	.bottom-left {
		border-bottom-left-radius: 85%; 
		background: #FF8135;
	}
	.bottom-right {
		border-bottom-right-radius: 85%; 
		background: #f85508;
	}
</style>