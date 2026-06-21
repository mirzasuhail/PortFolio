<script>
	const projects = [
		{ 
			id: 'riq', 
			code: 'RIQ', 
			num: '#01-07', 
			name: 'ResumeIQ', 
			role: 'AI SaaS / Backend', 
			desc: 'AI-powered resume analyzer & recruiter matching platform', 
			tech: 'React, Node.js, Gemini AI, TailwindCSS', 
			video: '/videos/ResumeIQ.mp4', 
			mobile_thumb: '/images/mobile_thumbnails/ResumeIQ.jpg',
			link: 'https://github.com/mirzasuhail/ResumeIQ' 
		},
		{ 
			id: 'vnx', 
			code: 'VNX', 
			num: '#02-07', 
			name: 'Vulnix', 
			role: 'DevSecOps CLI', 
			desc: 'AI-powered DevSecOps CLI for network vulnerability analysis', 
			tech: 'Python, Nmap, Gemini API, Typer, Rich', 
			video: '/videos/vulnix.mp4', 
			mobile_thumb: '/images/mobile_thumbnails/Vulnix.png',
			link: 'https://github.com/mirzasuhail/Vulnix' 
		},
		{ 
			id: 'ala', 
			code: 'ALA', 
			num: '#03-07', 
			name: 'AI Learning Arena', 
			role: 'AI Assistant', 
			desc: 'AI-Powered Learning Assistant for personalized education & quizzes', 
			tech: 'Python, OpenAI API, NLP, Flask', 
			video: null, 
			mobile_thumb: '/images/mobile_thumbnails/AILearningArena.png',
			link: 'https://github.com/mirzasuhail/AI-Powered-Learning-Assistant' 
		},
		{ 
			id: 'ksm', 
			code: 'KSM', 
			num: '#04-07', 
			name: 'KisanMitra', 
			role: 'ML SaaS / Flask', 
			desc: 'Agriculture-focused AI application for soil analysis and crop health', 
			tech: 'Python, ML, Flask, OpenCV', 
			video: '/videos/KisanMitra.mp4', 
			mobile_thumb: null,
			link: '#' 
		},
		{ 
			id: 'sdb', 
			code: 'SDB', 
			num: '#05-07', 
			name: 'Student Database', 
			role: 'Database System', 
			desc: 'Full-featured student database management and academic analysis system', 
			tech: 'Python, MySQL, Tkinter', 
			video: '/videos/StudentDatabaseManagementSystems.mp4', 
			mobile_thumb: '/images/mobile_thumbnails/StudentDatabaseManagement.png',
			link: '#' 
		},
		{ 
			id: 'prtb', 
			code: 'PRB', 
			num: '#06-07', 
			name: 'Blue Portfolio', 
			role: 'Web Development', 
			desc: 'Personal portfolio website with high-end editorial layouts and a dark/blue glassmorphism theme.', 
			tech: 'Next.js, Tailwind, Framer Motion', 
			video: '/videos/mirzaSuhailBluePortfolio.mp4', 
			mobile_thumb: '/images/mobile_thumbnails/BluePortfolio.jpg',
			link: 'https://github.com/mirzasuhail/mirzasuhailPortfolio' 
		},
		{ 
			id: 'prty', 
			code: 'PRY', 
			num: '#07-07', 
			name: 'Yellow Portfolio', 
			role: 'Web Development', 
			desc: 'Minimalist editorial portfolio featuring clean typography, structured layout, and a high-contrast yellow/beige highlight palette.', 
			tech: 'Next.js, Tailwind, Framer Motion', 
			video: '/videos/mirzaSuhailYellowPortfolio.mp4', 
			mobile_thumb: '/images/mobile_thumbnails/YellowPortfolio.png',
			link: 'https://github.com/mirzasuhail/mirzasuhailPortfolio' 
		}
	];

	const skills = [
		'Python, JavaScript, Java, C/C++',
		'React, Flask, FastAPI, Streamlit',
		'TensorFlow, PyTorch, Scikit-learn',
		'OpenCV, NumPy, Pandas, Matplotlib',
		'Git, Docker, Vercel, Render',
		'HTML5, CSS3, TailwindCSS',
	];

	const values = [
		'AI-driven problem solving',
		'Clean, scalable architecture',
		'Performance & optimization',
		'Mobile-first responsive design',
		'Open source contributor',
		'Continuous learning',
	];

	const certifications = [
		{
			title: 'Quantum Fundamentals',
			org: 'Qubitech / QKD BB84 Protocol',
			img: '/images/certifications/quantum.jpeg',
			url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Flms-cdn.qubitech.io%2Fmedia%2Fcertificates%2F1%2Fd7be267b%2F3c7e6d75_0ae7fa2d.jpg&urlhash=q__e&mt=Uip1Y60J-zM582hYY97_YUNR0ANTH67tcPVoVkJe5Az2f28t-Bsy2KWwXKPFx04aCE0khatmf62zcDp6pkAV7a9_Ouik&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3Bp%2Bwx7x%2FASBa%2BlOLAa2LuAg%3D%3D'
		},
		{
			title: 'SQL Basic',
			org: 'HackerRank',
			img: '/images/certifications/sqlbasic.jpeg',
			url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Fwww.hackerrank.com%2Fcertificates%2Fdd2cfd24e5e9&urlhash=If0h&mt=A5Ldcq1n8Wsyl3IO9ld0PfmCXts_Cwkc123W5H51hqsAKkcA65jqbqC9vyFVrEHAMdAO1k3ByB3aRC1j56lY8_p-BX-d&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3Bp%2Bwx7x%2FASBa%2BlOLAa2LuAg%3D%3D'
		},
		{
			title: 'Python Basic',
			org: 'HackerRank',
			img: '/images/certifications/python.jpeg',
			url: 'https://www.linkedin.com/safety/go/?url=https%3A%2F%2Fwww.hackerrank.com%2Fcertificates%2Ff55a547724f9&urlhash=HSdB&mt=KGE7S9LgvJUG9mJgtPnEVtK876n5BNPSFQ4ozTRXQ0QVC9l1Fg0aubrJA_-aZAqpEIRlquiYDbUHC44yEAJJcQBLCZKu&isSdui=true&lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3Bp%2Bwx7x%2FASBa%2BlOLAa2LuAg%3D%3D'
		},
		{
			title: 'Introduction to Artificial Intelligence',
			org: 'LinkedIn Learning',
			img: '/images/certifications/linkedinai.jpeg',
			url: 'https://www.linkedin.com/learning/certificates/fcdb9e1a7ec1741ac302e5955aebd8c596e0b26aafdd542a29c19124cad13cf4/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_certifications_details%3Bp%2Bwx7x%2FASBa%2BlOLAa2LuAg%3D%3D'
		},
		{
			title: 'Introduction to Artificial Intelligence (NASBA CPE)',
			org: 'LinkedIn Learning / NASBA',
			img: '/images/certifications/nasba.jpeg',
			url: 'https://www.linkedin.com/learning/certificates/e5c14dbd2d02cfac6f0326c3ec1fa3e37d882b36a395ab7707b008f29151f93a'
		},
		{
			title: 'Master Data Management for Beginners',
			org: 'TCS iON',
			img: '/images/certifications/tcsion.jpeg',
			url: '#'
		}
	];

	let activeProjectIndex = $state(0);
	let theme = $state('dark');
	let showScrollTop = $state(false);
	let activeModalImage = $state(null);

	// Sync theme state with layout/localStorage (defaults to dark on load)
	$effect(() => {
		theme = 'dark';
		document.documentElement.dataset.theme = 'dark';
	});

	function toggleTheme() {
		theme = theme === 'light' ? 'dark' : 'light';
		document.documentElement.dataset.theme = theme;
		localStorage.setItem('theme', theme);
	}

	// Scroll handler for showing the scroll-to-top button
	$effect(() => {
		function handleScroll() {
			showScrollTop = window.scrollY > 400;
		}
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});

	function scrollToTop() {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	}

	// Intersection Observer for fade-in sections
	$effect(() => {
		const sections = document.querySelectorAll('.fade-section');
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					if (entry.isIntersecting) {
						entry.target.classList.add('visible');
					}
				});
			},
			{ threshold: 0.08 }
		);
		sections.forEach((section) => observer.observe(section));
		return () => observer.disconnect();
	});

	// Scroll spy to highlight active project in the sticky list
	$effect(() => {
		const cards = document.querySelectorAll('.project-card');
		const observer = new IntersectionObserver(
			(entries) => {
				entries.forEach((entry) => {
					if (entry.isIntersecting) {
						const index = parseInt(entry.target.getAttribute('data-index') || '0', 10);
						activeProjectIndex = index;
					}
				});
			},
			{ threshold: 0.4, rootMargin: '-10% 0px -40% 0px' }
		);
		cards.forEach((card) => observer.observe(card));
		return () => observer.disconnect();
	});

	/**
	 * @param {string} id
	 */
	function scrollToProject(id) {
		const element = document.getElementById(id);
		if (element) {
			element.scrollIntoView({ behavior: 'smooth', block: 'center' });
		}
	}

	/**
	 * @param {string} link
	 */
	function handleProjectClick(link) {
		if (link && link !== '#') {
			window.open(link, '_blank');
		}
	}
</script>

<!-- ============ FLOATING SCROLL TO TOP BUTTON ============ -->
<button 
	class="scroll-to-top" 
	class:visible={showScrollTop} 
	onclick={scrollToTop} 
	aria-label="Back to top"
>
	↑
</button>

<!-- ============ SECTION 1: HERO ============ -->
<section id="home" class="hero">
	<video
		class="hero-video"
		src="/videos/Hero.mp4"
		autoplay
		loop
		muted
		playsinline
	></video>
	<div class="hero-overlay"></div>
	
	<div class="hero-wrapper container">
		<!-- Giant horizontal header MIRZA stretching edge to edge like SHELBY -->
		<div class="hero-header-container">
			<h1 class="hero-title-top anim-fade-up">
				<span>M</span>
				<span>I</span>
				<span>R</span>
				<span>Z</span>
				<span>A</span>
			</h1>
			
			<!-- SUHAIL positioned directly under MIRZA, aligned right, shifted upwards -->
			<div class="hero-title-sub-row anim-fade-up" style="animation-delay: 0.25s">
				<span class="hero-name-sub">SUHAIL</span>
			</div>
		</div>
		
		<!-- Sub-layout below MIRZA / SUHAIL -->
		<div class="hero-body-grid anim-fade-up" style="animation-delay: 0.4s">
			<!-- Tagline & Description -->
			<div class="hero-left-desc">
				<div class="hero-mid-row">
					<p class="hero-tagline">
						Backend Engineer &ensp;·&ensp; AI SaaS Developer &ensp;·&ensp; Web Developer
					</p>
					<div class="hero-badges">
						<a 
							href="https://www.credly.com/users/mirzasuhail" 
							target="_blank" 
							rel="noopener noreferrer" 
							class="hero-badge-btn"
						>
							Credly Profile &ensp;↗
						</a>
						<a 
							href="https://www.skills.google/public_profiles/547a5a16-6206-47be-bc8c-e59557f6ad56" 
							target="_blank" 
							rel="noopener noreferrer" 
							class="hero-badge-btn"
						>
							Google Skills Profile &ensp;↗
						</a>
					</div>
				</div>
				<p class="hero-desc">
					Focusing on engineering intelligent backend pipelines, designing robust system architectures, and crafting digital experiences with an editorial, unique approach.
				</p>
			</div>
		</div>

		<!-- Bottom layout footer containing nav links, social redirect links, theme toggle, and year -->
		<div class="hero-footer anim-fade-up" style="animation-delay: 0.6s">
			<div class="hero-nav-links">
				<a href="#work">Work</a>
				<a href="#profile">Profile</a>
				<a href="#contact">Contact</a>
				<span class="nav-divider">|</span>
				<a href="https://github.com/mirzasuhail" target="_blank" rel="noopener noreferrer">GitHub</a>
				<a href="https://linkedin.com/in/mirzasuhail" target="_blank" rel="noopener noreferrer">LinkedIn</a>
				<button 
					class="theme-toggle-inline" 
					onclick={toggleTheme}
					aria-label="Toggle theme"
				>
					{theme === 'dark' ? '☀' : '●'}
				</button>
			</div>
			<div class="hero-year">
				<span>2026</span>
			</div>
		</div>
	</div>
</section>

<!-- ============ SECTION 2: WORK ============ -->
<section id="work" class="section-work fade-section">
	<div class="container work-container">
		<p class="section-label sticky-label">Selected Work</p>
		
		<div class="work-split">
			<!-- Sticky Left Column: Project Titles List -->
			<div class="work-list-sticky">
				<div class="project-links-list">
					{#each projects as project, i}
						<button
							class="project-link-item"
							class:active={activeProjectIndex === i}
							onclick={() => scrollToProject(project.id)}
						>
							{project.name}
						</button>
					{/each}
				</div>
			</div>
			
			<!-- Scrolling Right Column: Dedicated Project Cards with Videos -->
			<div class="work-grid-scrolling">
				{#each projects as project, i}
					<div 
						class="project-card" 
						id={project.id} 
						data-index={i}
					>
						<div class="card-layout">
							<!-- Left metadata label vertically aligned -->
							<div class="card-meta">
								<span class="card-num">{project.num}</span>
							</div>
							
							<!-- Main video showcase box displaying fully -->
							<div class="card-media-wrapper">
								{#if project.video}
									<video 
										class="card-video" 
										src={project.video} 
										poster={project.mobile_thumb || null}
										autoplay 
										loop 
										muted 
										playsinline
									></video>
								{:else}
									<img 
										src={project.mobile_thumb || '/images/ai_learning_arena.png'} 
										alt={project.name} 
										class="card-image-full" 
									/>
								{/if}
							</div>
						</div>
						
						<!-- Dedicated project details block below the video -->
						<div class="card-details">
							<div class="details-header">
								<span class="details-code">{project.code}</span>
								<h3 class="details-name">{project.name}</h3>
								{#if project.link !== '#'}
									<button 
										class="details-btn" 
										onclick={() => handleProjectClick(project.link)}
									>
										Code →
									</button>
								{/if}
							</div>
							<p class="details-desc">{project.desc}</p>
							<div class="details-tech">
								{#each project.tech.split(', ') as tag}
									<span class="tech-tag">{tag}</span>
								{/each}
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<!-- ============ SECTION 3: PROFILE ============ -->
<section id="profile" class="section-profile fade-section">
	<div class="container">
		<p class="section-label">Developer Profile</p>
		
		<div class="profile-about-block">
			<h2 class="profile-title">Developer Profile</h2>
			<p class="profile-bio-text">
				I am Mohammad Mirza Suhail, an AIML specialist and Backend Software Engineer based in India. I specialize in designing robust backend pipelines, deploying machine learning systems, and engineering custom AI SaaS products.
			</p>
			<p class="profile-bio-text">
				Bringing technical discipline from computer engineering and electromechanical systems, I develop intelligent software designed to scale cleanly while maintaining high code reliability standards.
			</p>
		</div>

		<div class="profile-grid">
			<!-- Skills -->
			<div class="profile-col">
				<h3 class="profile-subheading">Technical Stack</h3>
				<ul class="profile-list">
					{#each skills as skill}
						<li class="profile-list-item">{skill}</li>
					{/each}
				</ul>
			</div>
			
			<!-- Core Values -->
			<div class="profile-col">
				<h3 class="profile-subheading">Values &amp; Methodology</h3>
				<ul class="profile-list">
					{#each values as value}
						<li class="profile-list-item">{value}</li>
					{/each}
				</ul>
			</div>
		</div>

		<!-- Certifications Card Grid -->
		<div class="background-section">
			<h3 class="profile-subheading">Certifications</h3>
			
			<div class="certifications-grid">
				{#each certifications as cert}
					<div class="cert-card">
						<!-- svelte-ignore a11y_click_events_have_key_events -->
						<!-- svelte-ignore a11y_no_static_element_interactions -->
						<div 
							class="cert-image-box" 
							onclick={() => activeModalImage = cert.img} 
							style="cursor: pointer;"
						>
							<img src={cert.img} alt={cert.title} class="cert-img" />
						</div>
						<div class="cert-info">
							<span class="cert-org">{cert.org}</span>
							<h4 class="cert-title">{cert.title}</h4>
							<a 
								href={cert.url} 
								target="_blank" 
								rel="noopener noreferrer" 
								class="cert-credential-link"
							>
								Credential Link &ensp;→
							</a>
						</div>
					</div>
				{/each}
			</div>

			<!-- Public Badges and Profiles Row (Moved to Hero Section) -->
		</div>

		<!-- Experience Section -->
		<div class="background-section">
			<h3 class="profile-subheading">Professional Experience</h3>
			
			<div class="experience-block">
				<div class="experience-header">
					<div class="exp-role-company">
						<span class="exp-company">Aaviza Electronics Pvt. Ltd., Bangalore</span>
						<h4 class="exp-role">Industrial Trainee / Trainee Intern</h4>
					</div>
					<span class="exp-date">Nov 2023 – May 2024</span>
				</div>
				<div class="exp-description">
					<p>
						Completed a comprehensive six-month industrial training program, gaining hands-on exposure to production systems, electronic assembly, PCB assembly, soldering techniques, and quality control systems within ISO 9001 and AS9100-certified environments.
					</p>
					<ul class="exp-bullets">
						<li>Worked across high-reliability divisions including **Aerospace** and **Hitachi**, learning lean manufacturing and component reliability protocols.</li>
						<li>Supported Shop Floor operations on industrial products for key clients: **Sun Mobility**, **Larsen &amp; Toubro (L&amp;T)**, and **Ametek**.</li>
						<li>Gained deep knowledge of electromechanical assembly practices, quality control checkpoints, product validation, and technical documentation.</li>
					</ul>
				</div>
			</div>
		</div>

		<!-- Education Section -->
		<div class="background-section">
			<h3 class="profile-subheading">Education</h3>
			<div class="background-table">
				<div class="table-row">
					<span class="table-cell title">B.Tech in Artificial Intelligence &amp; Machine Learning</span>
					<span class="table-cell org">Annamacharya Institute of Technology, based in India</span>
					<span class="table-cell date">2024–2027</span>
				</div>
				<div class="table-row border-last">
					<span class="table-cell title">Diploma in Computer Engineering</span>
					<span class="table-cell org">Govt Polytechnic College, Puttur (Score: 83%)</span>
					<span class="table-cell date">2021–2024</span>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- ============ SECTION 4: CONTACT ============ -->
<section id="contact" class="section-contact fade-section">
	<div class="container contact-inner">
		<p class="contact-sublabel">Get in touch</p>
		<div class="contact-title">
			<div>SAY HELLO</div>
			<div class="at-symbol">@</div>
			<div>MIRZASUHAIL.IN</div>
		</div>
		<a href="mailto:mirzasuhail.in@gmail.com" class="contact-action-btn">
			mirzasuhail.in@gmail.com
		</a>
		<p class="contact-location">Based in India 🇮🇳 &ensp;·&ensp; Available for opportunities</p>
		
		<div class="social-links">
			<a href="https://github.com/mirzasuhail" target="_blank" rel="noopener noreferrer">GitHub</a>
			<a href="https://linkedin.com/in/mirzasuhail" target="_blank" rel="noopener noreferrer">LinkedIn</a>
			<a href="https://twitter.com/mirzasuhail" target="_blank" rel="noopener noreferrer">Twitter</a>
		</div>
	</div>
</section>

{#if activeModalImage}
	<!-- svelte-ignore a11y_click_events_have_key_events -->
	<!-- svelte-ignore a11y_no_static_element_interactions -->
	<div 
		class="lightbox-modal" 
		onclick={() => activeModalImage = null}
	>
		<button class="lightbox-close" onclick={() => activeModalImage = null}>&times;</button>
		<!-- svelte-ignore a11y_no_noninteractive_element_interactions -->
		<img 
			src={activeModalImage} 
			alt="Enlarged Certificate" 
			class="lightbox-img" 
			onclick={(e) => e.stopPropagation()} 
		/>
	</div>
{/if}

<style>
	/* ====== FLOATING SCROLL TO TOP ====== */
	.scroll-to-top {
		position: fixed;
		bottom: 2rem;
		right: 2rem;
		width: 3.5rem;
		height: 3.5rem;
		border-radius: 50%;
		background: var(--text);
		color: var(--bg);
		border: 1px solid var(--border);
		cursor: pointer;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 1.5rem;
		z-index: 1000;
		opacity: 0;
		transform: translateY(20px);
		transition: opacity 0.4s cubic-bezier(0.16, 1, 0.3, 1), transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
		pointer-events: none;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
	}

	.scroll-to-top.visible {
		opacity: 0.8;
		transform: translateY(0);
		pointer-events: auto;
	}

	.scroll-to-top:hover {
		opacity: 1;
		transform: scale(1.05);
	}

	/* ====== HERO ====== */
	.hero {
		position: relative;
		width: 100%;
		height: 100vh;
		min-height: 650px;
		overflow: hidden;
		background: var(--bg);
		display: flex;
		align-items: center;
		transition: background-color 0.5s cubic-bezier(0.16, 1, 0.3, 1);
	}

	.hero-video {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		z-index: 0;
		opacity: 0.2; /* 80% background visibility, 20% video opacity */
		filter: grayscale(1) contrast(1.15) brightness(1.0); /* sharp, high-contrast, gray video texture */
	}

	.hero-overlay {
		position: absolute;
		inset: 0;
		z-index: 1;
		background: transparent;
	}

	.hero-wrapper {
		position: relative;
		z-index: 2;
		width: 100%;
		display: flex;
		flex-direction: column;
		height: 100%;
		justify-content: space-between;
		padding-top: 5rem;
		padding-bottom: 3rem;
	}

	/* Giant horizontal header MIRZA stretching edge to edge like SHELBY */
	.hero-header-container {
		width: 100%;
		display: flex;
		flex-direction: column;
		position: relative;
	}

	.hero-title-top {
		font-family: 'Ranade', sans-serif;
		font-size: clamp(3rem, 15vw, 15rem);
		font-weight: 700;
		text-transform: uppercase;
		line-height: 0.9;
		color: var(--text);
		margin: 0;
		width: 100%;
		display: flex;
		justify-content: space-between;
	}

	.hero-title-sub-row {
		width: 100%;
		display: flex;
		justify-content: flex-start; /* left-aligned with description and MIRZA start */
		margin-top: 0.5rem; /* a clean gap below MIRZA to prevent collision */
	}

	/* Smaller SUHAIL positioned directly under MIRZA, aligned right, shifted upwards */
	.hero-name-sub {
		font-family: 'Ranade', sans-serif;
		font-size: clamp(2rem, 7.5vw, 5.8rem);
		font-weight: 700;
		text-transform: uppercase;
		line-height: 0.85;
		color: var(--text);
		letter-spacing: 0.12em; /* adds slight letter-spacing gap */
	}

	/* Sub-layout below MIRZA / SUHAIL */
	.hero-body-grid {
		display: flex;
		flex-direction: column;
		gap: 3rem;
		width: 100%;
		margin-top: 2rem;
	}

	.hero-left-desc {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
		max-width: 1100px;
		width: 100%;
	}

	.hero-mid-row {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		gap: 2rem;
	}

	.hero-badges {
		display: flex;
		gap: 1.5rem;
		align-items: center;
	}

	.hero-badge-btn {
		display: inline-flex;
		align-items: center;
		padding: 0.8rem 1.8rem;
		border: 1px solid var(--border);
		border-radius: 100px;
		font-size: 0.85rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		transition: background-color 0.3s, color 0.3s, transform 0.3s;
		color: var(--text);
		white-space: nowrap;
		cursor: pointer;
	}

	.hero-badge-btn:hover {
		background: var(--text);
		color: var(--bg);
		transform: translateY(-2px);
		opacity: 1;
	}

	.hero-tagline {
		font-family: 'Ranade', sans-serif;
		font-size: clamp(0.95rem, 1.3vw, 1.15rem);
		font-weight: 700;
		letter-spacing: 0.08em;
		text-transform: uppercase;
		color: var(--text);
	}

	.hero-desc {
		font-size: clamp(1.1rem, 2vw, 1.45rem);
		line-height: 1.45;
		font-weight: 350;
		opacity: 0.85;
		color: var(--text);
	}

	/* Hero footer with Navigation Links and Inline Theme Toggle under the name */
	.hero-footer {
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 0.85rem;
		font-weight: 700;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		border-top: 1px solid var(--border);
		padding-top: 1.5rem;
		margin-top: auto;
	}

	.hero-nav-links {
		display: flex;
		align-items: center;
		flex-wrap: wrap;
		gap: 2.2rem;
	}

	.hero-nav-links a {
		text-decoration: none;
		color: var(--text);
		opacity: 0.65;
		transition: opacity 0.3s;
	}

	.hero-nav-links a:hover {
		opacity: 1;
	}

	.nav-divider {
		opacity: 0.25;
		font-weight: 300;
	}

	.theme-toggle-inline {
		background: none;
		border: none;
		font-size: 1.05rem;
		cursor: pointer;
		color: var(--text);
		opacity: 0.65;
		padding: 0;
		margin: 0;
		line-height: 1;
		transition: opacity 0.3s, transform 0.3s;
	}

	.theme-toggle-inline:hover {
		opacity: 1;
		transform: scale(1.15);
	}

	.hero-year {
		color: var(--text);
		opacity: 0.65;
	}

	/* Hero Entrance Animation */
	.anim-fade-up {
		opacity: 0;
		transform: translateY(20px);
		animation: fadeInUp 1.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;
	}

	/* ====== SECTION LABELS ====== */
	.section-label {
		font-size: 0.8rem;
		letter-spacing: 0.15em;
		text-transform: uppercase;
		opacity: 0.45;
		color: var(--text);
		font-weight: 700;
	}

	/* ====== WORK ====== */
	.section-work {
		padding: 8rem 0;
	}

	.work-container {
		display: flex;
		flex-direction: column;
		gap: 3rem;
	}

	.work-split {
		display: grid;
		grid-template-columns: 1fr 2fr;
		gap: 4rem;
		position: relative;
	}

	.work-list-sticky {
		position: sticky;
		top: 6rem;
		height: fit-content;
	}

	.project-links-list {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		gap: 1.2rem;
	}

	.project-link-item {
		background: none;
		border: 1px solid transparent;
		border-radius: 4px;
		padding: 0.2rem 0.6rem;
		font-family: 'Ranade', sans-serif;
		font-size: clamp(1.5rem, 2.5vw, 2.4rem);
		font-weight: 700;
		color: var(--text);
		opacity: 0.25;
		cursor: pointer;
		text-align: left;
		transition: opacity 0.4s cubic-bezier(0.16, 1, 0.3, 1), border-color 0.4s ease, transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
		white-space: nowrap;
	}

	.project-link-item:hover, .project-link-item.active {
		opacity: 1;
		transform: translateX(8px);
	}

	.project-link-item.active {
		border-color: var(--text);
	}

	/* Scrolling Column project cards */
	.work-grid-scrolling {
		display: flex;
		flex-direction: column;
		gap: 10rem;
	}

	.project-card {
		display: flex;
		flex-direction: column;
		width: 100%;
	}

	.card-layout {
		display: flex;
		align-items: flex-start;
		gap: 2rem;
	}

	.card-meta {
		display: flex;
		flex-direction: column;
		padding-top: 0.5rem;
	}

	.card-num {
		font-size: 0.85rem;
		font-weight: 600;
		opacity: 0.45;
		writing-mode: vertical-rl;
		transform: rotate(180deg);
		letter-spacing: 0.1em;
	}

	.card-media-wrapper {
		flex: 1;
		border-radius: 4px;
		overflow: hidden;
		background: rgba(0, 0, 0, 0.05);
		border: 1px solid var(--border);
		box-shadow: 0 10px 30px rgba(0,0,0,0.02);
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: auto;
	}

	.card-video {
		width: 100%;
		height: auto;
		display: block;
		object-fit: contain; /* displays fully with no cropping */
	}

	.card-image-full {
		width: 100%;
		height: auto;
		display: block;
		object-fit: contain;
	}





	/* Card Details block */
	.card-details {
		margin-top: 2rem;
		padding-left: 3.2rem; /* aligns exactly with the video starting edge */
	}

	.details-header {
		display: flex;
		align-items: center;
		gap: 1.5rem;
		margin-bottom: 1rem;
	}

	.details-code {
		font-size: 0.8rem;
		font-family: 'SF Mono', 'Fira Code', monospace;
		opacity: 0.4;
		border: 1px solid var(--border);
		padding: 0.2rem 0.5rem;
		border-radius: 3px;
	}

	.details-name {
		font-size: clamp(1.5rem, 2.5vw, 2.4rem);
		font-weight: 700;
		color: var(--text);
		margin: 0;
	}

	.details-btn {
		background: none;
		border: none;
		font-size: 0.9rem;
		font-weight: 600;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		color: var(--text);
		cursor: pointer;
		opacity: 0.5;
		transition: opacity 0.3s, transform 0.3s;
		padding: 0;
	}

	.details-btn:hover {
		opacity: 1;
		transform: translateX(4px);
	}

	.details-desc {
		font-size: clamp(1rem, 1.4vw, 1.25rem);
		line-height: 1.6;
		opacity: 0.75;
		margin-bottom: 1.5rem;
		max-width: 700px;
	}

	.details-tech {
		display: flex;
		flex-wrap: wrap;
		gap: 0.6rem;
	}

	.tech-tag {
		font-size: 0.8rem;
		font-weight: 500;
		border: 1px solid var(--border);
		padding: 0.3rem 0.8rem;
		border-radius: 100px;
		opacity: 0.75;
		color: var(--text);
	}

	/* ====== PROFILE ====== */
	.section-profile {
		padding: 8rem 0;
		border-top: 1px solid var(--border);
	}

	.profile-about-block {
		margin-bottom: 5rem;
		max-width: 900px;
	}

	.profile-title {
		font-size: clamp(2.2rem, 4.5vw, 3.8rem);
		font-weight: 700;
		margin-bottom: 1.8rem;
		color: var(--text);
	}

	.profile-bio-text {
		font-size: clamp(1.1rem, 1.8vw, 1.35rem);
		line-height: 1.6;
		opacity: 0.85;
		color: var(--text);
		margin-bottom: 1.5rem;
	}

	.profile-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 6rem;
	}

	.profile-subheading {
		font-size: clamp(1.3rem, 2.2vw, 2rem);
		font-weight: 700;
		margin-bottom: 2rem;
		color: var(--text);
		border-bottom: 1px solid var(--border);
		padding-bottom: 0.8rem;
	}

	.profile-list {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
	}

	.profile-list-item {
		font-size: 1.1rem;
		padding-bottom: 0.8rem;
		border-bottom: 1px solid var(--border);
		opacity: 0.75;
		color: var(--text);
		font-weight: 350;
	}

	/* Certifications Card Grid */
	.certifications-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
		gap: 2.5rem;
		margin-bottom: 3.5rem;
	}

	.cert-card {
		display: flex;
		flex-direction: column;
		background: rgba(0, 0, 0, 0.01);
		border: 1px solid var(--border);
		border-radius: 8px;
		overflow: hidden;
		transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.3s;
	}

	.cert-card:hover {
		transform: translateY(-4px);
		box-shadow: 0 10px 20px rgba(0,0,0,0.03);
	}

	.cert-image-box {
		width: 100%;
		height: auto;
		display: block;
		background: rgba(0, 0, 0, 0.02);
		padding: 0;
		border-bottom: 1px solid var(--border);
	}

	.cert-img {
		width: 100%;
		height: auto;
		display: block;
	}

	/* ====== LIGHTBOX MODAL ====== */
	.lightbox-modal {
		position: fixed;
		inset: 0;
		background: rgba(0, 0, 0, 0.95);
		z-index: 2000;
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 2rem;
		cursor: pointer;
		animation: fadeIn 0.2s cubic-bezier(0.16, 1, 0.3, 1) forwards;
	}

	.lightbox-close {
		position: absolute;
		top: 1.5rem;
		right: 2rem;
		background: none;
		border: none;
		color: #fff;
		font-size: 3rem;
		cursor: pointer;
		opacity: 0.7;
		transition: opacity 0.3s;
		z-index: 2001;
	}

	.lightbox-close:hover {
		opacity: 1;
	}

	.lightbox-img {
		width: 90%;
		max-width: 1200px;
		height: auto;
		max-height: 85vh;
		object-fit: contain;
		border-radius: 4px;
		box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
		animation: scaleUp 0.25s cubic-bezier(0.16, 1, 0.3, 1) forwards;
		cursor: default;
	}

	@keyframes scaleUp {
		from {
			transform: scale(0.96);
			opacity: 0;
		}
		to {
			transform: scale(1);
			opacity: 1;
		}
	}

	.cert-info {
		padding: 1.5rem;
		display: flex;
		flex-direction: column;
		gap: 0.4rem;
	}

	.cert-org {
		font-size: 0.75rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		opacity: 0.5;
	}

	.cert-title {
		font-size: 1.15rem;
		font-weight: 700;
		color: var(--text);
		margin: 0;
		line-height: 1.3;
	}

	.cert-credential-link {
		font-size: 0.85rem;
		font-weight: 700;
		color: var(--text);
		opacity: 0.7;
		margin-top: 0.8rem;
		text-decoration: none;
		transition: opacity 0.3s, transform 0.3s;
		display: inline-block;
		width: fit-content;
	}

	.cert-credential-link:hover {
		opacity: 1;
		transform: translateX(4px);
	}

	/* Profile link badges moved to Hero Section */

	/* Experience Section Detail blocks */
	.experience-block {
		display: flex;
		flex-direction: column;
		gap: 1.5rem;
		border-bottom: 1px solid var(--border);
		padding-bottom: 3rem;
		margin-bottom: 2rem;
	}

	.experience-header {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		gap: 2rem;
	}

	.exp-role-company {
		display: flex;
		flex-direction: column;
		gap: 0.3rem;
	}

	.exp-company {
		font-size: 0.9rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.08em;
		opacity: 0.5;
	}

	.exp-role {
		font-size: clamp(1.4rem, 2.5vw, 2.1rem);
		font-weight: 700;
		color: var(--text);
		margin: 0;
	}

	.exp-date {
		font-size: 0.95rem;
		opacity: 0.65;
		font-weight: 500;
	}

	.exp-description {
		font-size: 1.15rem;
		line-height: 1.6;
		opacity: 0.85;
		max-width: 900px;
	}

	.exp-bullets {
		margin-top: 1.2rem;
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
		list-style: square;
		padding-left: 1.5rem;
	}

	.exp-bullets li {
		line-height: 1.55;
	}

	/* Background structural table */
	.background-section {
		margin-top: 6rem;
	}

	.background-table {
		display: flex;
		flex-direction: column;
		border-top: 1px solid var(--border);
	}

	.table-row {
		display: grid;
		grid-template-columns: 1.8fr 2fr 1fr;
		padding: 2.2rem 0;
		border-bottom: 1px solid var(--border);
		font-size: 1.05rem;
		color: var(--text);
	}

	.table-cell.title {
		font-weight: 700;
	}

	.table-cell.org {
		opacity: 0.65;
	}

	.table-cell.date {
		text-align: right;
		opacity: 0.5;
	}

	/* ====== CONTACT ====== */
	.section-contact {
		padding: 0 0 8rem;
		width: 100%;
	}

	.contact-inner {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		background: #5e6d61; /* solid grayish green matching screenshot */
		padding: 10rem 2rem;
		border-radius: 8px;
		color: #f5f0eb;
	}

	:global([data-theme='dark']) .contact-inner {
		background: #252b26;
	}

	.contact-sublabel {
		font-size: 0.75rem;
		letter-spacing: 0.15em;
		text-transform: uppercase;
		opacity: 0.65;
		font-weight: 700;
		margin-bottom: 3.5rem;
	}

	.contact-title {
		font-size: clamp(2.2rem, 8vw, 7.5rem);
		font-weight: 700;
		text-transform: uppercase;
		line-height: 0.9;
		letter-spacing: -0.02em;
		margin-bottom: 4rem;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.at-symbol {
		font-family: 'Source Serif 4', serif;
		font-style: italic;
		font-weight: 300;
		margin: 0.5rem 0;
		opacity: 0.8;
	}

	.contact-action-btn {
		font-size: clamp(1.2rem, 2vw, 1.8rem);
		font-weight: 500;
		text-decoration: none;
		border: 1px solid rgba(245, 240, 235, 0.3);
		padding: 1rem 2.5rem;
		border-radius: 100px;
		transition: background-color 0.3s, color 0.3s, border-color 0.3s;
		color: #f5f0eb;
		margin-bottom: 2rem;
	}

	.contact-action-btn:hover {
		background: #f5f0eb;
		color: #5e6d61;
		border-color: #f5f0eb;
		opacity: 1;
	}

	.contact-location {
		font-size: 0.9rem;
		opacity: 0.6;
		margin-top: 1rem;
		letter-spacing: 0.05em;
		text-transform: uppercase;
	}

	.section-contact .social-links {
		display: flex;
		gap: 3rem;
		margin-top: 5rem;
	}

	.section-contact .social-links a {
		font-size: 0.9rem;
		opacity: 0.6;
		transition: opacity 0.3s ease;
		color: #f5f0eb;
		text-transform: uppercase;
		letter-spacing: 0.1em;
	}

	.section-contact .social-links a:hover {
		opacity: 1;
	}

	/* ====== FADE-IN ANIMATION ====== */
	.fade-section {
		opacity: 0;
		transform: translateY(40px);
		transition: opacity 1.2s cubic-bezier(0.16, 1, 0.3, 1), transform 1.2s cubic-bezier(0.16, 1, 0.3, 1);
	}

	:global(.fade-section.visible) {
		opacity: 1;
		transform: translateY(0);
	}

	/* ====== RESPONSIVE ====== */
	@media (max-width: 992px) {
		.fade-section {
			opacity: 1 !important;
			transform: none !important;
			transition: none !important;
		}

		.card-media-wrapper {
			display: flex !important;
			width: 100%;
			max-width: 320px;
			margin: 0;
			height: auto;
			flex: none;
			border-radius: 4px;
			overflow: hidden;
			border: 1px solid var(--border);
			background: rgba(0, 0, 0, 0.05);
		}

		.work-split {
			grid-template-columns: 1fr;
			gap: 3rem;
		}

		.work-list-sticky {
			position: sticky;
			top: 0;
			z-index: 100;
			background: var(--bg);
			padding-top: 1rem;
			padding-bottom: 0.5rem;
			border-bottom: 1px solid var(--border);
			margin-left: calc(-1 * clamp(1.5rem, 6vw, 5rem));
			margin-right: calc(-1 * clamp(1.5rem, 6vw, 5rem));
			padding-left: clamp(1.5rem, 6vw, 5rem);
			padding-right: clamp(1.5rem, 6vw, 5rem);
			backdrop-filter: blur(10px);
			background: color-mix(in srgb, var(--bg) 95%, transparent);
		}

		.project-links-list {
			display: flex;
			flex-direction: row;
			flex-wrap: wrap;
			justify-content: flex-start;
			gap: 0.8rem 1.2rem;
			padding-bottom: 0.5rem;
			width: 100%;
		}

		.project-link-item {
			font-size: 1.15rem;
			transform: none !important; /* disable hover translation on mobile */
			padding: 0.15rem 0.5rem;
		}

		.work-grid-scrolling {
			gap: 6rem;
		}

		.experience-header {
			flex-direction: column;
			gap: 0.5rem;
		}

		.exp-date {
			margin-top: 0.2rem;
		}

		.table-row {
			grid-template-columns: 1fr;
			gap: 0.5rem;
			padding: 1.5rem 0;
		}

		.table-cell.date {
			text-align: left;
			margin-top: 0.25rem;
		}
	}

	@media (max-width: 768px) {
		.hero {
			flex-direction: column;
			justify-content: center;
			align-items: stretch;
		}

		.certifications-grid {
			grid-template-columns: 1fr;
			gap: 1.5rem;
		}

		.hero-wrapper {
			padding-top: 3.5rem;
			padding-bottom: 2.5rem;
		}

		/* MIRZA SUHAIL layout for Mobile View */
		.hero-title-top {
			font-size: clamp(2.8rem, 15vw, 8rem);
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			width: 100%;
			margin-top: 0rem;
		}

		.hero-title-sub-row {
			order: 0;
			width: 100%;
			justify-content: flex-start;
			margin-top: 0.5rem;
		}

		.hero-name-sub {
			font-size: clamp(1.5rem, 7.5vw, 3.2rem);
			letter-spacing: 0.12em;
		}

		.hero-body-grid {
			display: flex;
			flex-direction: column;
			align-items: flex-start;
			margin-top: 1rem;
		}

		.hero-left-desc {
			display: flex;
			flex-direction: column;
			max-width: 100%;
		}

		.hero-mid-row {
			display: contents;
		}

		.hero-tagline {
			order: 1;
		}

		.hero-desc {
			order: 2;
			margin-top: 0.5rem;
		}

		.hero-badges {
			order: 3;
			display: flex;
			flex-direction: column;
			align-items: flex-start;
			gap: 0.8rem;
			width: 100%;
			margin-top: 1.5rem;
		}

		.hero-badge-btn {
			justify-content: center;
		}

		.hero-badges .hero-badge-btn:nth-child(1) {
			width: 50%;
		}

		.hero-badges .hero-badge-btn:nth-child(2) {
			width: 75%;
		}

		.hero-footer {
			flex-direction: column;
			align-items: flex-start;
			gap: 1.2rem;
			padding-top: 1rem;
		}

		.hero-nav-links {
			width: 100%;
			justify-content: space-between;
			gap: 1rem;
		}

		.profile-grid {
			grid-template-columns: 1fr;
			gap: 3rem;
		}

		.section-work {
			padding: 5rem 0;
		}

		.section-profile {
			padding: 5rem 0;
		}

		.background-section {
			margin-top: 4rem;
		}

		.card-layout {
			flex-direction: column;
			gap: 1rem;
			align-items: flex-start;
		}

		.card-num {
			writing-mode: horizontal-tb;
			transform: none;
		}

		.card-details {
			padding-left: 0;
			margin-top: 1.5rem;
		}
	}
</style>
