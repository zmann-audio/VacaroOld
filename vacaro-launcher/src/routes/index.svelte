<script>
	import {
		Grid,
		Row,
		Column,
		Tile,
		AspectRatio,
		ButtonSet,
		Dropdown,
		Button
	} from 'carbon-components-svelte';
	import Launch from 'carbon-icons-svelte/lib/Launch.svelte';
	import FAQ from '../components/home/FAQ.svelte';
	import YT from '../components/home/YT.svelte';
</script>

<Tile style="height: 400px;">
	<Grid>
		<Row>
			<Column>Column</Column>
			<Column>Column</Column>
			<Column>Column</Column>
			<Column sm={{ offset: 10 }} >
				<ButtonSet stacked>
					<Button icon={Launch}>Launch Engine</Button>
					<Dropdown
						hideLabel
						light
						warn
						warnText="Warning, the Vacaro Launcher is still in early development."
						type="default"
						style="width: 100%;"
						titleText="Engine Version"
						selectedId="0"
						items={[
							{ id: '0', text: '0.0.1' },
							{ id: '1', text: '0.0.2 Beta' },
							{ id: '2', text: '0.0.3 Alpha' }
						]}
					/>
				</ButtonSet>
			</Column>
		</Row>
	</Grid>
</Tile>

<Grid style="margin-top: 12px; width: 100%;">
	<Row>
		<Column aspectRatio="2x1">
			<AspectRatio ratio="16x9">
				<Tile style="height: 100% !important;">
					<YT title="Music" url="https://www.youtube.com/embed/_8_X-M68c6Q" />
				</Tile>
			</AspectRatio>
		</Column>
		<Column aspectRatio="2x1">
			<FAQ />
		</Column>
	</Row>
</Grid>
