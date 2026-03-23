![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat)
![Vibe Coded](https://img.shields.io/static/v1?message=Vibe%20Coded&labelColor=5c5c5c&color=7c3aed&logoColor=white&label=%20&style=for-the-badge)

# Chris Willcutt — Personal Landing Page

*Project title — update if reusing this template.*

A personal landing page built to showcase my analytics skills, projects, and professional background to recruiters and hiring managers. It exists because a resume alone cannot communicate the depth of a technical project — this site gives context, detail, and a direct way to get in touch. It is designed for hiring teams at corporate and consulting companies looking for data analyst or business analyst candidates in Chicago and the broader Midwest.

## Features

*List the key things a visitor or recruiter will experience on the page.*

- Professional hero section with circular headshot, name, and analytics-focused tagline
- Skills displayed as grouped, color-coded pill badges across three categories: Tools, Visualization, and Techniques
- Project cards with descriptions drawn from real coursework (MLB regression analysis, Oracle APEX database, Python web scraping)
- Work experience section with role, organization, location, dates, and bullet-point achievements
- Click-to-contact section with direct links to LinkedIn, email, and GitHub
- Sticky navigation bar with smooth-scroll anchor links to every section
- Fully responsive layout — single column on mobile, two-column project grid on desktop
- Accessible design meeting WCAG 2.2 Level AA standards

## Tech Stack

*Update the table to match your actual tools if reusing this template.*

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and semantic markup |
| CSS3 | All styling, layout, and responsive design |
| Google Fonts (Inter) | Typography — loaded via CDN |
| Python `http.server` | Local development server (development only) |

## Getting Started

### Prerequisites

*List everything a contributor needs before they can run the project locally.*

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- [Python 3](https://www.python.org/downloads/) — only required if you want to run a local dev server; the site is otherwise plain HTML/CSS

### Installation

*Step-by-step commands to get the project running locally. Update the repo URL if reusing.*

1. Clone the repository:

```bash
git clone https://github.com/Cjwillcutt/3300-landing-page.git
```

2. Navigate into the project folder:

```bash
cd 3300-landing-page
```

3. Start a local web server on port 5000:

```bash
python3 -m http.server 5000
```

4. Open your browser and go to:

```
http://localhost:5000
```

The site will load immediately — no build step or package installation required.

## Usage

*Explain how a visitor uses the site once it is running.*

Open `index.html` in a browser (or visit the hosted URL) to view the full landing page. Use the sticky navigation bar at the top to jump between sections: About, Skills, Projects, Experience, and Contact. All external links (LinkedIn, GitHub) open in a new tab. The contact section includes a direct email link.

To customize the content for your own use, edit `index.html` with your own name, bio, skills, projects, and experience, and update `css/stylesheet.css` to change colors, fonts, or layout. No configuration files or environment variables are needed.

## Project Structure

*Update file comments if you add or remove files when reusing this template.*

```
3300-landing-page/
├── index.html                        # Main single-page HTML file — all content lives here
├── css/
│   └── stylesheet.css                # All styles — no inline CSS anywhere in the project
├── js/                               # JavaScript directory — reserved for future scripts
├── Images/
│   └── Image1.jpg                    # Professional headshot displayed in the hero section
├── PRD.md                            # Product Requirements Document defining goals and content
├── STANDARDS.md                      # Technical and design standards for this project
├── README.md                         # This file
└── Christopher Willcutt Resume.pdf   # Source resume used as content reference (not linked in site)
```

## Changelog

*Add a new entry here each time you release a new version.*

### v1.0.0 — March 23, 2026

- Initial release of personal landing page
- Sticky navigation with smooth-scroll anchor links
- Hero section with circular headshot, name, and tagline
- About Me section with bio, Dean's List mention, and target market
- Skills section with pill badges grouped into Tools, Visualization, and Techniques
- Three project cards: MLB regression analysis, MLB Oracle APEX database, Car Value web scraping
- Professional experience section covering three roles (2022–2025)
- Contact section with LinkedIn, email, and GitHub links
- Fully responsive layout from 320px and wider
- Deployment configured as a static site

## Known Issues / To-Do

*Check off items as you complete them. Add new ones as you discover them.*

- [ ] Car Value Analysis project card has a brief description — add more detail once the project is documented
- [ ] No JavaScript interactivity — project filter or section fade-in animations could improve the experience
- [ ] No favicon — a small branded icon should be added for browser tab and bookmark display
- [ ] The `js/scripts.js` file does not exist yet — the directory is reserved but empty
- [ ] Form-based contact option (e.g., a mailto form) would reduce friction compared to raw email link

## Roadmap

*Future improvements for a hypothetical next version.*

- Add a downloadable resume button that links to a hosted PDF
- Build a filterable project gallery as the number of projects grows
- Add subtle scroll-triggered animations using the Intersection Observer API
- Create a dark mode toggle using CSS custom properties
- Expand to a multi-page site with a dedicated Projects page once more work is complete

## Contributing

*Update the repo URL if reusing this template.*

This is a personal project, but suggestions and improvements are welcome. To contribute, fork the repository, make your changes on a new branch, and open a pull request with a clear description of what you changed and why.

1. Fork the repository on GitHub
2. Create a new branch: `git checkout -b your-feature-name`
3. Make your changes and commit them: `git commit -m "Describe your change"`
4. Push to your fork: `git push origin your-feature-name`
5. Open a pull request against the `main` branch of this repository

Please follow the conventions in `STANDARDS.md` — no inline styles, semantic HTML only, and all images need descriptive alt text.

## License

This project is licensed under the [MIT License](LICENSE).

## Author

*Update with your name, institution, and course if reusing this template.*

**Chris Willcutt**
University of Iowa — Tippie College of Business
BAIS:3300 — Digital Product Management, Module 8

## Contact

- GitHub: [github.com/Cjwillcutt](https://github.com/Cjwillcutt/3300-landing-page)
- LinkedIn: [linkedin.com/in/christopher-j-willcutt](https://www.linkedin.com/in/christopher-j-willcutt)
- Email: [Chrisjwillcutt@gmail.com](mailto:Chrisjwillcutt@gmail.com)

## Acknowledgements

- [Google Fonts](https://fonts.google.com/) — Inter typeface used throughout the site
- [shields.io](https://shields.io/) — Badge generation for the README header
- [WCAG 2.2 Guidelines](https://www.w3.org/WAI/WCAG22/quickref/) — Accessibility reference used to meet Level AA requirements
- [MDN Web Docs](https://developer.mozilla.org/) — Reference for HTML5 semantic elements and CSS layout
- Replit AI Agent — Initial HTML structure, CSS stylesheet, and README generated with Replit Agent and reviewed, tested, and approved by the author
- Icon: [vibe coding](https://thenounproject.com) by iqonica from [Noun Project](https://thenounproject.com) (CC BY 3.0)
