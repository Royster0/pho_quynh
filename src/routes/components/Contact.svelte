<section class="contact" id="contact">
	<div class="container">
		<h2>Contact Us</h2>
		<p><span>Address:</span> 31434 Pacific Hwy S, Federal Way, WA 98003</p>
		<p><span>Phone:</span> (253) 529-2241</p>
		<div class="business-hours">
			<h3>Business Hours</h3>
			<div class="hours-list">
				<div>Monday:</div>
				<div>9:30 AM - 9:30 PM</div>
				<div>Tuesday:</div>
				<div>9:30 AM - 9:30 PM</div>
				<div>Wednesday:</div>
				<div>9:30 AM - 9:30 PM</div>
				<div>Thursday:</div>
				<div>9:30 AM - 10:00 PM</div>
				<div>Friday:</div>
				<div>9:30 AM - 10:00 PM</div>
				<div>Saturday:</div>
				<div>9:30 AM - 10:00 PM</div>
				<div>Sunday:</div>
				<div>9:30 AM - 10:00 PM</div>
			</div>
		</div>
	</div>

	<iframe
		src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5409.473563040683!2d-122.31862934289914!3d47.319480512714414!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x5490577a2a28e07f%3A0x4da4f84f392bcc40!2zUGjhu58gUXXhu7NuaCBSZXN0YXVyYW50!5e0!3m2!1sen!2sus!4v1722344349420!5m2!1sen!2sus"
		width="600"
		height="450"
		style="border:0;"
		allowfullscreen=""
		loading="lazy"
		referrerpolicy="no-referrer-when-downgrade"
	></iframe>
</section>

<style>
	.contact {
		padding: 80px 20px;
		text-align: center;
		background-color: #1a1a1a;
	}

	.contact h2 {
		font-size: 2.5rem;
		margin-bottom: 20px;
		color: #d0b457;
	}

	.contact p {
		font-size: 1.2rem;
		color: #f3f3f3;
	}

	span {
		font-weight: 600;
	}

	.business-hours {
		margin-top: 40px;
	}

	.business-hours h3 {
		font-size: 2rem;
		color: #d0b457;
		margin-bottom: 20px;
	}

	.hours-list {
		display: grid;
		grid-template-columns: 1fr 1fr;
		max-width: 400px;
		margin: 0 auto;
		text-align: left;
		gap: 10px 20px;
	}

	.hours-list div {
		font-size: 1.2rem;
		color: #f3f3f3;
	}

	iframe {
		margin-top: 40px;
	}

	@media (max-width: 768px) {
		.hours-list {
			grid-template-columns: 1fr;
		}

		.hours-list div {
			text-align: center;
		}

		.contact h2 {
			font-size: 2rem;
		}

		.contact p,
		.business-hours h3,
		.hours-list div {
			font-size: 1rem;
		}
	}
</style>
