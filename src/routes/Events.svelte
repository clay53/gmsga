<svelte:head>
    <title>Upcoming Events - Governor Mifflin High School Student Government Association</title>
    <meta name="description" content="A list of all of the upcoming events for the Governor Mifflin High School Student Government Association with basic information. Events include powder puff, wreaths across america, and mini-thon." />
    <link rel="canonical" href="https://gmsga.com/events" />
</svelte:head>

<script lang="ts">
    import Event from "../components/Event.svelte";
</script>

<h1>Upcoming Events</h1>
<div>
    <Event title="Powder Puff" date="November 9th, 2021" color="black" bg="#fcd4f7" to="/powder-puff" />
    <Event title="Wreaths Across America" date="October 19th, 2021" color="black" bg="#86d980" to="/wreaths-across-america" />
    <Event title="Mini-THON" date="April 1st, 2022" color="black" bg="#eb88a9" to="/mini-thon" />
</div>