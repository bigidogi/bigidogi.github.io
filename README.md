<!DOCTYPE html>
<html lang="en">
<head>
	<meta name="description" content="Special Event Calculator">
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Kanit:ital,wght@300;500;700;800;900&family=Lobster&display=swap" rel="stylesheet">

	<style>
		html {
			font-size: 62.5%;
		}
		body {
			background-color: #4d004d;
			color: #ffffff;
			margin: 0;
			padding: 1rem;
		}
		header {
			font-family: 'Kanit', sans-serif;
			font-weight: 900;
			font-style: italic;
			font-size: 3rem;
			text-align: center;
		}
		h1 {
			font-family: 'Kanit', sans-serif;
			font-weight: 800;
			font-style: italic;
			font-size: 2rem;
			text-align: center;
			margin-bottom: 3rem;
		}
		h2 {
			font-family: 'Kanit', sans-serif;
			font-weight: 700;
			font-style: italic;
			font-size: 1.5rem;
			text-align: center;
		}
		.globalColumn {
			display: flex;
			justify-content: space-between;
			align-items: flex-start;
			gap: 1rem;
			margin: 0 2rem;
		}
		.column {
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			align-items: center;
			gap: 1rem;
			margin: 0 2rem;
		}
		.container {
			display: flex;
			justify-content: space-between;
			align-items: flex-start;
			gap: 2rem;
		}
		.dropdown {
			display: flex;
			justify-content: space-between;
			align-items: center;
			width: 30vw;
		}
		select {
			font-family: 'Kanit', sans-serif;
			font-weight: 300;
			font-style: italic;
			font-size: 1rem;
			color:lightgray;
			text-align: center;
			border-radius: 0.5rem;
			background-color: #610061;
			border: none;
			height: 2rem;
			width: 10rem;
			transition: background-color 0.3s ease;
			touch-action: manipulation;
		}
		select:hover {
			background-color: #750075;
		}
		p {
			font-family: 'Kanit', sans-serif;
			font-weight: 500;
			font-style: italic;
			font-size: 1.5rem;
			text-align: right;
			height: 2rem;
			}
		.choose {
			font-family: 'Kanit', sans-serif;
			font-weight: 300;
			font-style: italic;
			color: lightgray;
		}
		.locked {
			font-family: 'Kanit', sans-serif;
			font-weight: 300;
			font-style: italic;
			color: red;
		}
		.star {
			font-family: 'Kanit', sans-serif;
			font-weight: 300;
			font-style: italic;
			color: orange;
		}
		lineV {
			width: 3px;
			height: 39rem;
			background-color: #610061;
			margin: 1rem 0;
		}
		a {
			font-family: 'Kanit', sans-serif;
			font-weight: 500;
			font-style: italic;
			font-size: 1.5rem;
			color: #ffc6c2;
			text-align: right;
			height: 2rem;
			transition: color 0.3s ease;
		}
		a:hover {
			color: white;
		}
		img {
			transition: filter 0.3s ease;
			filter: grayscale(2);
		}
		img:hover {
			filter: none;
		}

		@media (max-width: 767px) {
			html {
				font-size: 50%;
			}
			body {
				background-color: #4d004d;
				color: #ffffff;
				margin: 0;
				padding: 1rem;
			}
			header {
				font-family: 'Kanit', sans-serif;
				font-weight: 900;
				font-style: italic;
				font-size: 3rem;
				text-align: center;
			}
			h1 {
				font-family: 'Kanit', sans-serif;
				font-weight: 800;
				font-style: italic;
				font-size: 2rem;
				text-align: center;
				margin-bottom: 1rem;
			}
			h2 {
				font-family: 'Kanit', sans-serif;
				font-weight: 700;
				font-style: italic;
				font-size: 1.5rem;
				text-align: center;
			}
			.globalColumn {
				display: flex;
				flex-direction: column;
				justify-content: space-between;
				align-items: center;
				gap: 1rem;
				margin: 0 2rem;
			}
			.column {
				display: flex;
				flex-direction: column;
				justify-content: space-between;
				align-items: center;
				gap: 1rem;
			}
			.container {
				display: flex;
				justify-content: space-between;
				align-items: flex-start;
				gap: 1rem;
			}
			.dropdown {
				display: flex;
				flex-direction: column;
				justify-content: flex-start;
				align-items: center;
				width: 40vw;
			}
			select {
				font-family: 'Kanit', sans-serif;
				font-weight: 300;
				font-style: italic;
				font-size: 1rem;
				color:lightgray;
				text-align: center;
				border-radius: 0.5rem;
				background-color: #610061;
				border: none;
				height: 2rem;
				width: 10rem;
				transition: background-color 0.3s ease;
				touch-action: manipulation;
			}
			select:hover {
				background-color: #750075;
			}
			p {
				font-family: 'Kanit', sans-serif;
				font-weight: 500;
				font-style: italic;
				font-size: 1.5rem;
				text-align: right;
				height: 1.5rem;
				}
			.choose {
				font-family: 'Kanit', sans-serif;
				font-weight: 300;
				font-style: italic;
				color: lightgray;
			}
			.locked {
				font-family: 'Kanit', sans-serif;
				font-weight: 300;
				font-style: italic;
				color: red;
			}
			.star {
				font-family: 'Kanit', sans-serif;
				font-weight: 300;
				font-style: italic;
				color: orange;
			}
			lineV {
				width: 80vw;
				height: 3px;
				background-color: #610061;
				margin: 2rem 0;
			}
			a {
				font-family: 'Kanit', sans-serif;
				font-weight: 500;
				font-style: italic;
				font-size: 1.5rem;
				color: #ffc6c2;
				text-align: right;
				height: 1.5rem;	
				transition: color 0.3s ease;
			}
			a:hover {
				color: white;
			}
			img {
				transition: filter 0.3s ease;
				filter: grayscale(1);
			}
			img:hover {
				filter: none;
			}
	</style>
</head>
<body>
	<header>Bugatti Mistral</header>
	<h1>Special Event Calculator</h1>
	<div class="globalColumn">
		<div class="container">
			<div class="column">
				<div class="dropdown">
					<p>Team Fordzilla P1</p>
						<select id="car1" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Jaguar XJR-9</p>
						<select id="car2" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Zenvo Aurora Tur</p>
						<select id="car3" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>W Motors Lykan Neon</p>
						<select id="car4" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Torino Design Super Sport</p>
						<select id="car5" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Deus Vayanne</p>
						<select id="car6" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
							<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Bugatti Mistral</p>
					<select id="car13" required onchange="selectColor(this)">
						<option class="choose" value="0" disabled selected>Stars</option>
						<option class="locked" value="0">Locked</option>
						<option class="star" value="1">&starf;</option>
						<option class="star" value="2">&starf;&starf;</option>
						<option class="star" value="3">&starf;&starf;&starf;</option>
						<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
						<option class="star" value="6">&starf;&starf;&starf;&starf;&starf;&starf;</option>
					</select>
				</div>
			</div>
			<div class="column">
				<div class="dropdown">
					<p>Aston Martin Vulcan</p>
						<select id="car7" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Nissan GT-R Nismo</p>
						<select id="car8" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Ferrari J50</p>
						<select id="car9" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Icona Vulcano Titanium</p>
						<select id="car10" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>Ferrari FXX K</p>
						<select id="car11" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
				<div class="dropdown">
					<p>W Motors Lykan</p>
						<select id="car12" required onchange="selectColor(this)">
							<option class="choose" value="0" disabled selected>Stars</option>
							<option class="locked" value="0">Locked</option>
							<option class="star" value="1">&starf;</option>
							<option class="star" value="2">&starf;&starf;</option>
							<option class="star" value="3">&starf;&starf;&starf;</option>
							<option class="star" value="4">&starf;&starf;&starf;&starf;</option>
							<option class="star" value="5">&starf;&starf;&starf;&starf;&starf;</option>
						</select>
				</div>
			</div>
		</div>
		<lineV></lineV>
		<div class="container" style="width: 50vw">
			<div class="column" style="align-items: flex-start">
				<p>Conditions:</p>
				<p>End Stage:</p>
				<p>Credits:</p>
				<p>Tokens:</p>
				<p>Blueprints:</p>
				<p>EIP:</p>
				<p id="res7"></p>
			</div>
			<div class="column" id="results" style="align-items: flex-end">
				<p id="res1">0</p>
				<p id="res2">1</p>
				<p id="res3">0</p>
				<p id="res4">0</p>
				<p id="res5">0</p>
				<p id="res6">0</p>
			</div>
		</div>
	</div>
	<div style=" display:flex; justify-content:space-between; align-items:center; margin: 2rem 4rem">
		<div style=" display:flex; justify-content:flex-start; align-items:center;">
			<p>Created by</p>
			<a href="https://discord.com/users/426439047540375553" target="_blank">Drugoy/BigiDogi</a>
		</div>
		<a href="https://t.me/asphalt_9legends" target="_blank" style="height: 5rem">
			<img src="tg_a.png" style="height: 5rem">
		</a>
	</div>
	<script>
function selectColor(selectElement) {
	const selectedOption = selectElement.options[selectElement.selectedIndex];
	selectElement.className = selectedOption.className;
	let currentStage = 1;
    let currentConditions = 0;
    let currentRewards = [
        { RewardID: 1, Count: 0 },
        { RewardID: 2, Count: 0 },
        { RewardID: 3, Count: 0 },
        { RewardID: 4, Count: 0 },
        { RewardID: 5, Count: 0 },
        { RewardID: 6, Count: 0 },
        { RewardID: 7, Count: 0 },
        { RewardID: 8, Count: 0 },
		{ RewardID: 9, Count: 0 },
    ];

    const cars = [
        parseInt(document.getElementById("car1").value) || 0,
        parseInt(document.getElementById("car2").value) || 0,
        parseInt(document.getElementById("car3").value) || 0,
        parseInt(document.getElementById("car4").value) || 0,
        parseInt(document.getElementById("car5").value) || 0,
        parseInt(document.getElementById("car6").value) || 0,
        parseInt(document.getElementById("car7").value) || 0,
        parseInt(document.getElementById("car8").value) || 0,
        parseInt(document.getElementById("car9").value) || 0,
        parseInt(document.getElementById("car10").value) || 0,
        parseInt(document.getElementById("car11").value) || 0,
        parseInt(document.getElementById("car12").value) || 0,
        parseInt(document.getElementById("car13").value) || 0,
    ];

  const stages = [
  { Stage_Number: 1, Unlock: 0 },
  { Stage_Number: 2, Unlock: 10 },
  { Stage_Number: 3, Unlock: 25 },
  { Stage_Number: 4, Unlock: 45 },
  { Stage_Number: 5, Unlock: 70 },
  { Stage_Number: 6, Unlock: 100 },
  { Stage_Number: 7, Unlock: 125 },
  { Stage_Number: 8, Unlock: 150 },
  { Stage_Number: 9, Unlock: 175 },
  { Stage_Number: 10, Unlock: 200 },
  { Stage_Number: 11, Unlock: 225 },
  { Stage_Number: 12, Unlock: 250 },
  { Stage_Number: 13, Unlock: 275 },
  { Stage_Number: 14, Unlock: 280 },
  { Stage_Number: 15, Unlock: 290 },
  { Stage_Number: 16, Unlock: 300 },
  { Stage_Number: 17, Unlock: 300 },
  ];

  const rewards = [
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 2, RewardID: 1, Reward_Count: 30000, Multiply: 4},
  {Stage_Number: 1, CarID: 1, AnyID: 0, Min_Stars: 2, RewardID: 2, Reward_Count: 10, Multiply: 3},
  {Stage_Number: 1, CarID: 1, AnyID: 7, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 1, CarID: 1, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 1, Reward_Count: 30000, Multiply: 5},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 2, RewardID: 1, Reward_Count: 35000, Multiply: 4},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 2, RewardID: 2, Reward_Count: 15, Multiply: 3},
  {Stage_Number: 2, CarID: 2, AnyID: 0, Min_Stars: 2, RewardID: 5, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 2, CarID: 2, AnyID: 8, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 2, CarID: 2, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 3, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 3, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 3, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 1, Reward_Count: 50000, Multiply: 5},
  {Stage_Number: 3, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 2, Reward_Count: 25, Multiply: 5},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 1, Reward_Count: 35000, Multiply: 5},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 2, RewardID: 1, Reward_Count: 40000, Multiply: 4},
  {Stage_Number: 4, CarID: 3, AnyID: 0, Min_Stars: 2, RewardID: 2, Reward_Count: 20, Multiply: 3},
  {Stage_Number: 4, CarID: 3, AnyID: 9, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 4, CarID: 3, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 1, Reward_Count: 40000, Multiply: 5},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 2, RewardID: 1, Reward_Count: 45000, Multiply: 4},
  {Stage_Number: 5, CarID: 4, AnyID: 0, Min_Stars: 2, RewardID: 2, Reward_Count: 25, Multiply: 3},
  {Stage_Number: 5, CarID: 4, AnyID: 10, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 5, CarID: 4, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 6, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 6, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 6, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 1, Reward_Count: 60000, Multiply: 5},
  {Stage_Number: 6, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 2, Reward_Count: 35, Multiply: 5},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 1, Reward_Count: 45000, Multiply: 5},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 2, RewardID: 1, Reward_Count: 50000, Multiply: 4},
  {Stage_Number: 7, CarID: 5, AnyID: 0, Min_Stars: 2, RewardID: 2, Reward_Count: 30, Multiply: 3},
  {Stage_Number: 7, CarID: 5, AnyID: 11, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 7, CarID: 5, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 1, Reward_Count: 25000, Multiply: 5},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 1, Reward_Count: 50000, Multiply: 5},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 2, RewardID: 1, Reward_Count: 55000, Multiply: 4},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 2, RewardID: 2, Reward_Count: 35, Multiply: 3},
  {Stage_Number: 8, CarID: 6, AnyID: 0, Min_Stars: 2, RewardID: 5, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 8, CarID: 6, AnyID: 12, Min_Stars: 3, RewardID: 7, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 8, CarID: 6, AnyID: 0, Min_Stars: 3, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 9, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 9, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 9, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 1, Reward_Count: 75000, Multiply: 5},
  {Stage_Number: 9, CarID: 13, AnyID: 0, Min_Stars: 0, RewardID: 2, Reward_Count: 45, Multiply: 5},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 1, RewardID: 1, Reward_Count: 50000, Multiply: 5},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 4, RewardID: 1, Reward_Count: 50000, Multiply: 4},
  {Stage_Number: 10, CarID: 0, AnyID: 7, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 5, RewardID: 1, Reward_Count: 75000, Multiply: 3},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 5, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 5, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 6, RewardID: 2, Reward_Count: 40, Multiply: 3},
  {Stage_Number: 10, CarID: 1, AnyID: 7, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 1, RewardID: 1, Reward_Count: 50000, Multiply: 5},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 4, RewardID: 1, Reward_Count: 60000, Multiply: 4},
  {Stage_Number: 11, CarID: 0, AnyID: 8, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 5, RewardID: 1, Reward_Count: 85000, Multiply: 3},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 5, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 5, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 6, RewardID: 2, Reward_Count: 45, Multiply: 3},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 6, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 11, CarID: 2, AnyID: 8, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 1, RewardID: 1, Reward_Count: 50000, Multiply: 5},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 4, RewardID: 1, Reward_Count: 70000, Multiply: 4},
  {Stage_Number: 12, CarID: 0, AnyID: 9, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 5, RewardID: 1, Reward_Count: 95000, Multiply: 3},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 5, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 5, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 6, RewardID: 2, Reward_Count: 50, Multiply: 3},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 6, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 12, CarID: 3, AnyID: 9, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 1, RewardID: 1, Reward_Count: 60000, Multiply: 5},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 4, RewardID: 1, Reward_Count: 80000, Multiply: 4},
  {Stage_Number: 13, CarID: 4, AnyID: 0, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 2},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 5, RewardID: 1, Reward_Count: 100000, Multiply: 3},
  {Stage_Number: 13, CarID: 0, AnyID: 10, Min_Stars: 5, RewardID: 5, Reward_Count: 2, Multiply: 3},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 6, RewardID: 2, Reward_Count: 55, Multiply: 3},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 6, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 13, CarID: 4, AnyID: 10, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 1, RewardID: 1, Reward_Count: 60000, Multiply: 5},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 4, RewardID: 1, Reward_Count: 90000, Multiply: 4},
  {Stage_Number: 14, CarID: 5, AnyID: 0, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 3},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 5, RewardID: 1, Reward_Count: 110000, Multiply: 3},
  {Stage_Number: 14, CarID: 0, AnyID: 11, Min_Stars: 5, RewardID: 5, Reward_Count: 2, Multiply: 2},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 6, RewardID: 2, Reward_Count: 60, Multiply: 3},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 6, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 14, CarID: 5, AnyID: 11, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 1, RewardID: 1, Reward_Count: 60000, Multiply: 5},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 4, RewardID: 1, Reward_Count: 100000, Multiply: 4},
  {Stage_Number: 15, CarID: 6, AnyID: 0, Min_Stars: 4, RewardID: 5, Reward_Count: 1, Multiply: 2},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 5, RewardID: 1, Reward_Count: 120000, Multiply: 3},
  {Stage_Number: 15, CarID: 0, AnyID: 12, Min_Stars: 5, RewardID: 5, Reward_Count: 2, Multiply: 3},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 6, RewardID: 2, Reward_Count: 65, Multiply: 3},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 6, RewardID: 8, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 15, CarID: 6, AnyID: 12, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 1},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 1, RewardID: 3, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 1, RewardID: 4, Reward_Count: 1, Multiply: 5},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 1, RewardID: 1, Reward_Count: 80000, Multiply: 5},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 1, RewardID: 1, Reward_Count: 100000, Multiply: 5},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 2, RewardID: 2, Reward_Count: 50, Multiply: 5},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 3, RewardID: 1, Reward_Count: 150000, Multiply: 4},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 4, RewardID: 2, Reward_Count: 75, Multiply: 4},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 5, RewardID: 1, Reward_Count: 175000, Multiply: 3},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 6, RewardID: 2, Reward_Count: 100, Multiply: 3},
  {Stage_Number: 16, CarID: 13, AnyID: 0, Min_Stars: 6, RewardID: 6, Reward_Count: 1, Multiply: 2},
  ];
  const extraRewards = [
    { Conditions: 10, RewardID: 7, Reward_Count: 2 },
    { Conditions: 20, RewardID: 7, Reward_Count: 2 },
    { Conditions: 30, RewardID: 5, Reward_Count: 2 },
    { Conditions: 45, RewardID: 7, Reward_Count: 2 },
    { Conditions: 60, RewardID: 7, Reward_Count: 2 },
    { Conditions: 75, RewardID: 5, Reward_Count: 2 },
    { Conditions: 100, RewardID: 7, Reward_Count: 2 },
    { Conditions: 125, RewardID: 7, Reward_Count: 2 },
    { Conditions: 150, RewardID: 4, Reward_Count: 8 },
    { Conditions: 175, RewardID: 2, Reward_Count: 50 },
    { Conditions: 200, RewardID: 1, Reward_Count: 100000 },
    { Conditions: 250, RewardID: 5, Reward_Count: 3 },
    { Conditions: 300, RewardID: 6, Reward_Count: 1 },
    { Conditions: 350, RewardID: 1, Reward_Count: 200000 },
    { Conditions: 400, RewardID: 6, Reward_Count: 2 },
    { Conditions: 450, RewardID: 5, Reward_Count: 8 },
    { Conditions: 475, RewardID: 2, Reward_Count: 250 },
    { Conditions: 490, RewardID: 6, Reward_Count: 2 },
    { Conditions: 491, RewardID: 9, Reward_Count: 1 },
  ];

  const carMapping = {
    car1: 1,
    car2: 2,
    car3: 3,
    car4: 4,
    car5: 5,
    car6: 6,
    car7: 7,
    car8: 8,
    car9: 9,
    car10: 10,
    car11: 11,
    car12: 12,
    car13: 13,
  };
    while (true) {
        const stageData = stages.find((s) => s.Stage_Number === currentStage);
        if (!stageData || stageData.Unlock > currentConditions)  {
            break;
        }

        rewards
            .filter((r) => r.Stage_Number === currentStage)
            .forEach((reward) => {
                const carID = reward.CarID;
                if ((cars[carID - 1] !== undefined && reward.Min_Stars <= cars[carID - 1]) || (cars[reward.AnyID - 1] !== undefined && reward.Min_Stars <= cars[reward.AnyID - 1])) {
                    const rewardEntry = currentRewards.find(
                        (r) => r.RewardID === reward.RewardID
                    );
                    rewardEntry.Count += reward.Reward_Count * reward.Multiply;
                    currentConditions += reward.Multiply;
                }
            });

        currentStage++;
    }

    extraRewards.forEach((extraReward) => {
        if (extraReward.Conditions <= currentConditions) {
            const rewardEntry = currentRewards.find(
                (r) => r.RewardID === extraReward.RewardID
            );
            rewardEntry.Count += extraReward.Reward_Count;
        }
    });

    let specialMessage = "";
    if (currentConditions === 491) {
        specialMessage = "You'll get a Decal!";
	}

    const resultMap = {
        res1: `${currentConditions}`,
        res2: `${currentStage - 1}`,
        res3: `${currentRewards.find((r) => r.RewardID === 1).Count}`,
        res4: `${currentRewards.find((r) => r.RewardID === 2).Count}`,
        res5: `${currentRewards.find((r) => r.RewardID === 5).Count}`,
        res6: `${currentRewards.find((r) => r.RewardID === 6).Count}`,
		res7: specialMessage,
    };

    for (let id in resultMap) {
        const element = document.getElementById(id);
        if (element) {
            element.textContent = resultMap[id];
        } else {
            console.error(`Элемент с ID ${id} не найден.`);
        }
    }
};
	</script>
</body>