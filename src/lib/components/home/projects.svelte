<script>
	import Card from '../base/card.svelte';
	import Section from '../layout/section.svelte';
	import ProjectsGrid from '$lib/components/layout/projects-grid.svelte';
	import ThreeByThreeGrid from '$lib/components/layout/3x3-grid.svelte';
	import OneByOneGrid from '$lib/components/layout/1x1-grid.svelte';
	import ExternalLinkIcon from '$lib/svg/external-link.svelte';
	import Github from '$lib/svg/socials/github.svelte';
	import Blobs from '../layout/blobs.svelte';
	import Image from '../base/image.svelte';
	import Tag from '../base/tag.svelte';
</script>

<section id="projects">
	<Section
		align="top"
		title="Projects"
		description="I like to build some small projects when learning. Technologies are varied and so are their purposes. Most of them are open source!"
	>
		<OneByOneGrid>
			<ProjectsGrid>
				<Card>
					<div slot="image">
						<Image path="projects" filename="yatra" alt="Yatra" />
					</div>
					<div slot="content">
						<div class="title">
							Yatra Portal
							<div class="links">
								<a
									class="text-secondary"
									href="http://kptapp/yatra"
									target="_blank"
									rel="noopener"
									title="Open site"
								>
									<ExternalLinkIcon />
								</a>
							</div>
						</div>
						<div class="text">
							All tour proposal advances goes through this portal so that physical file movement can
							be avoided and the approval process becomes trackable and faster

							<!-- <a
								class="project-post-button button secondary-light transparent"
								href="/blog-development-sveltekit"
							>
								Read blog post
							</a> -->
						</div>
					</div>
					<div slot="footer">
						<div class="tags">
							<Tag>Angular</Tag>
							<Tag color="secondary">PHP</Tag>
						</div>
					</div>
				</Card>

				<Card>
					<div slot="image">
						<Image path="projects" filename="consumables" alt="Pocket Companion" />
					</div>
					<div slot="content">
						<div class="title">
							Consumables Dashboard
							<div class="links">
								<!-- <a
									class="text-secondary"
									href="https://github.com/itrasmi/acnh-pocket-companion"
									target="_blank"
									rel="noopener"
									title="Open project on GitHub"
								>
									<Github />
								</a> -->

								<a
									class="text-secondary"
									href="http://kptapp/consumables"
									target="_blank"
									rel="noopener"
									title="Open site"
								>
									<ExternalLinkIcon />
								</a>
							</div>
						</div>
						<div class="text">
							Dashboard for Consumables monitoring which reduces consumable wastage as well as
							shortage by improving planning.

							<!-- <a
								class="project-post-button button secondary-light transparent"
								href="/ionic-animal-crossing-companion"
							>
								Read blog post
							</a> -->
						</div>
					</div>
					<div slot="footer">
						<div class="tags">
							<Tag>Angular</Tag>
							<Tag>SASS</Tag>
							<Tag color="secondary">PHP</Tag>
						</div>
					</div>
				</Card>

				<Card>
					<div slot="image">
						<Image path="projects" filename="bus" alt="Gestek" />
					</div>
					<div slot="content">
						<div class="title">
							Bus Ticket Booking
							<div class="links">
								<a
									class="text-secondary"
									href="http://halkpt/folder_generation/bus_ticket_login.aspx"
									target="_blank"
									rel="noopener"
									title="Open site"
								>
									<ExternalLinkIcon />
								</a>
							</div>
						</div>
						<div class="text">Very useful connecting bus information.</div>
					</div>
					<div slot="footer">
						<div class="tags">
							<Tag>ASP.NET</Tag>
							<Tag>PWA</Tag>
						</div>
					</div>
				</Card>
			</ProjectsGrid>
			<!-- 
			<ThreeByThreeGrid>
				<Card>
					<div slot="image">
						<Image path="projects" filename="moneta" alt="Moneta" />
					</div>
					<div slot="content">
						<div class="title">
							Moneta
							<div class="links">
								<a
									class="text-secondary"
									href="https://github.com/itrasmi/moneta"
									target="_blank"
									rel="noopener"
									title="Open project on GitHub"
								>
									<Github />
								</a>

								<a
									class="text-secondary"
									href="https://appcenter.elementary.io/com.github.itrasmi.moneta/"
									target="_blank"
									rel="noopener"
									title="Open site"
								>
									<ExternalLinkIcon />
								</a>
							</div>
						</div>
						<div class="text">
							A desktop applet that displays currency rates and updates during the day. Built for
							elementary OS.
						</div>
					</div>
					<div slot="footer">
						<div class="tags">
							<Tag>Vala</Tag>
							<Tag>GTK</Tag>
							<Tag>Desktop</Tag>
							<Tag color="secondary">Open Source</Tag>
						</div>
					</div>
				</Card>

				<Card>
					<div slot="image">
						<Image path="projects" filename="reminduck" alt="Reminduck" />
					</div>
					<div slot="content">
						<div class="title">
							Reminduck
							<div class="links">
								<a
									class="text-secondary"
									href="https://github.com/itrasmi/reminduck"
									target="_blank"
									rel="noopener"
									title="Open project on GitHub"
								>
									<Github />
								</a>

								<a
									class="text-secondary"
									href="https://appcenter.elementary.io/com.github.itrasmi.reminduck/"
									target="_blank"
									rel="noopener"
									title="Open site"
								>
									<ExternalLinkIcon />
								</a>
							</div>
						</div>
						<div class="text">
							A simple reminder app for elementary OS, and my first experience writing native
							desktop apps.
						</div>
					</div>
					<div slot="footer">
						<div class="tags">
							<Tag>Vala</Tag>
							<Tag>GTK</Tag>
							<Tag>Desktop</Tag>
							<Tag color="secondary">Open Source</Tag>
						</div>
					</div>
				</Card>
			</ThreeByThreeGrid> -->
		</OneByOneGrid>
	</Section>
	<Blobs maxTop={5} minLeft={50} />
</section>

<style lang="scss">
	.title {
		display: flex;
		align-items: center;
		justify-content: space-between;
		.links {
			display: flex;
			align-items: center;
			justify-content: space-between;
			gap: 15px;
			a {
				width: 30px;
				height: 30px;
				padding: 3px;

				&:hover {
					color: var(--primary-color);
					fill: var(--primary-color);
				}
			}
		}
	}

	.project-post-button {
		width: fit-content;
		margin: 10px auto 0;
		font-weight: 500;
	}
</style>
