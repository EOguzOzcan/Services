<script>
  import { Col, Container, Row } from "sveltestrap";
  import Services from "./components/Services.svelte";
  import * as servicesDataText from "./data/servicesData.json";
  let servicesTextBundle = servicesDataText.default;
</script>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"
  />
</svelte:head>


<style>
.headBosluk{
    height: 100px;
}

.textBosluk{
    height: 100px;
}
.head {
    
    display: block;
    margin: auto;
    height: 150px;
	width: 800px;
    text-align: center;
    text-transform: uppercase;
    font-weight: bold;
    
}

.head h1 {
    font-size: 15px;
    height: 0px;
    font-size: x-large;
    
}

.header1 {
    margin-bottom: -14px;
    
}
.head h2 {
    
    opacity: 0.4;
    font-size: 80px;
    font-family: 'Oswald', sans-serif;
    
    
}

.behindContainer {
    
    position: relative;
    top: -70px;
}

.getBehind {
    position: absolute;
    width: 100%;
    height: auto;
    left: 6px;
    top: -5px;
    /* top: -3px; */
    display: block;
    z-index: 3;
    font-size: 65px;
    
    
}

.head3 {
    font-size: 15px;
    margin-top: 15px;
    font-family: 'Oswald', sans-serif;
    letter-spacing: 0.2em;
    
    
}
</style>

<Container>
		<div class="headBosluk"></div>
	<div class="head">
		<h1 class="header1">// 03</h1>
		<h2>what we do</h2>
		<div class="behindContainer">
		<div class="getBehind">services</div>
		</div>
		<div class="head3">DIGITAL TRANSFORMATION, BIG DATA, COMPUTER VISION, IOT, AI</div>
	</div>
	<div class="textBosluk"></div>

	<Row cols={2}>
	  {#each servicesTextBundle as services}
		<Col>
		  <Services
		  head={services.head}
		  servicesText={services.servicesText}
		  />
		</Col>
	  {/each}
	</Row>
  </Container>