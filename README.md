Personal Portfolio Website
A modern, responsive portfolio website showcasing skills, projects, and professional information with interactive UI elements and contact form integration.

Portfolio Preview

🌟 Features
Core Sections
Home/Hero Section: Eye-catching introduction with name, tagline, and profile photo
About Me: Personal summary highlighting passion, education, and interests
Skills: Multiple skill display formats:
Interactive hover cards with detailed descriptions
Animated CSS badges/pills
Animated progress bars showing proficiency levels
Projects: Responsive grid layout showcasing work with images and GitHub links
Education: Academic background and credentials
Resume: View and download resume options (local HTML + Google Drive)
Contact: Fully functional contact form with EmailJS integration
Technical Highlights
✅ Responsive Design: Works seamlessly on desktop, tablet, and mobile
✅ Smooth Scrolling: Anchor-based navigation with smooth scroll behavior
✅ Animated Elements:
Skill progress bars animate on scroll (Intersection Observer)
Hover effects on cards, buttons, and badges
Glassmorphism effects with backdrop-filter
✅ Form Validation: Client-side validation with real-time error messages
✅ Email Integration: Contact form sends emails via EmailJS
✅ Security: External links open in new tabs with rel="noopener noreferrer"
✅ Modern CSS: Flexbox, CSS Grid, custom properties, and advanced effects
🛠️ Technology Stack
Frontend
HTML5: Semantic markup
CSS3:
Flexbox for flexible layouts
CSS Grid for project cards
Custom badges/pills
Glassmorphism effects
Smooth transitions and animations
JavaScript (Vanilla ES6+):
Intersection Observer API for scroll animations
Form validation and error handling
EmailJS integration
Dynamic external link handling
Skills Demonstrated
Python (Pandas, NumPy, Flask, SQLite)
Web Development (HTML, CSS, JavaScript)
C Programming
Git version control
📁 Project Structure
personalpotfolio web/
├── port2.html          # Main portfolio page
├── README.md           # This file
static            
  ├── resume.html         # Printable resume page
  ├── background.jpg      # Background image
  ├── p.jpg               # Profile photo
  ├── home_page_sct.jpg   # Project 1 screenshot
  ├── image.png           # Project 2 screenshot
  └── (other assets)
🚀 Getting Started
Prerequisites
A modern web browser (Chrome, Firefox, Safari, Edge)
A local web server (Python, Node.js, or Live Server extension)
Installation
Clone or download this repository

git clone <your-repo-url>
cd personalpotfolio web
Start a local server

Option A: Python

python -m http.server 5000
Option B: Node.js (http-server)

npx http-server -p 5000
Option C: VS Code Live Server

Install "Live Server" extension
Right-click port2.html → "Open with Live Server"
Open in browser

http://localhost:5000/port2.html
⚙️ Configuration
EmailJS Setup (Contact Form)
Create EmailJS Account

Go to https://www.emailjs.com/
Sign up for a free account
Add Email Service

Dashboard → Email Services → Add New Service
Connect your email (Gmail, Outlook, etc.)
Note the Service ID (e.g., service_voriexv)
Create Email Template

Dashboard → Email Templates → Create New Template
Use this structure:
Subject: New Contact from {{from_name}}

Name: {{from_name}}
Email: {{reply_to}}

Message:
{{message}}
Note the Template ID (e.g., template_4xzb2ng)
Get Public Key

Dashboard → Account → General
Copy your Public Key (e.g., eGnljuifPkITJp0wh)
Update port2.html

// Line ~565: Update with your credentials
emailjs.init('YOUR_PUBLIC_KEY');

// Line ~597: Update service and template IDs
emailjs.send('YOUR_SERVICE_ID','YOUR_TEMPLATE_ID',{
  from_name: name,
  reply_to: email,
  message: message
})
Customization
Update Personal Information
Hero Section (Lines 368-379)

<h1>Your Name</h1>
<p1>I'm a <span style="color: #FFD700;">Your Title</span> Developer</p1>
Profile Photo (Line 378)

<img src="your-photo.jpg" alt="Profile">
About Section (Lines 383-390)

Replace with your own bio
Update interests list
Education (Lines 395-399)

Update institution name, degree, and years
Skills

Update skill cards (Lines 404-445)
Modify badges (Lines 448-459)
Adjust progress percentages (Lines 462-482)
Projects (Lines 486-513)

<div class="project-card">
  <img src="project-image.jpg" alt="Project Name" />
  <div class="project-body">
    <h4 class="project-title">Project Name</h4>
    <p class="project-desc">Description</p>
    <div class="project-links">
      <a class="btn" href="github-url">GitHub</a>
    </div>
  </div>
</div>
Resume Links (Lines 520-522)

Update Google Drive file IDs for your resume
Contact Info (Lines 555-557)

Update email, GitHub, and LinkedIn URLs
Color Scheme
Primary accent color (gold): #FFD700

/* Find and replace #FFD700 with your preferred color */
Background image:

body {
  background-image: url('your-background.jpg');
}
📝 Resume Page
The portfolio includes a separate printable resume page (resume.html):

Clean, print-friendly design
Separate sections: Summary, Skills, Projects, Education, Links
"Download PDF" button triggers browser print dialog
Organized skills by category:
Python (Pandas, NumPy, Standard Library)
Frameworks (Flask, Jinja2)
Database Management (SQLite, SQL)
Web Development (HTML, CSS, JavaScript)
Programming (C)
To update resume: Edit resume.html and modify the content in each section.

🎨 Design Features
Glassmorphism Effects
Cards use semi-transparent backgrounds with backdrop blur:

background-color: rgba(255, 255, 255, 0.15);
backdrop-filter: blur(10px);
Animated Progress Bars
Skills animate when scrolled into view using Intersection Observer API.

Hover Effects
Cards scale and glow on hover
Badges lift slightly
Buttons have smooth transitions
Responsive Grid
Projects use CSS Grid with auto-fit:

grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
🔒 Security
All external links automatically open in new tabs
Added rel="noopener noreferrer" for security
Form validation prevents XSS attacks
Email addresses are not exposed in frontend code
🐛 Troubleshooting
Contact Form Not Sending
Check EmailJS credentials are correct
Verify EmailJS account is active (free tier: 200 emails/month)
Open browser console (F12) to see error messages
Images Not Loading
Ensure image files are in the same directory as port2.html
Check file names match exactly (case-sensitive)
Use relative paths: image.jpg not ./image.jpg
Server Not Starting
# Check if port 5000 is already in use
netstat -ano | findstr :5000

# Use a different port
python -m http.server 8080
Progress Bars Not Animating
Ensure JavaScript is enabled
Check browser console for errors
Try clearing browser cache
📱 Browser Support
✅ Chrome 90+
✅ Firefox 88+
✅ Safari 14+
✅ Edge 90+
⚠️ Internet Explorer: Not supported (uses modern CSS features)
🚀 Deployment Options
GitHub Pages
Push to GitHub repository
Settings → Pages → Deploy from branch
Select main branch
Access at https://username.github.io/repo-name/port2.html
Netlify
Drag and drop folder to Netlify Drop
Or connect GitHub repo for continuous deployment
Vercel
npm i -g vercel
vercel
Custom Domain
Configure DNS settings with your hosting provider
Update EmailJS allowed domains if using custom domain
📄 License
This project is open source and available for personal and educational use.

👤 Author
Ganesh Karthik SL

GitHub: @Slganeshkarthik
LinkedIn: ganeshkarthik-sl
Email: slganeshkarthik@gamil.com
🙏 Acknowledgments
EmailJS for contact form functionality
Font Awesome for icons (if added)
Inspiration from modern portfolio designs
📊 Future Enhancements
 Add dark/light theme toggle
 Implement blog section
 Add certificate showcase
 Include testimonials section
 Integrate Google Analytics
 Add loading animations
 Create multilingual support
 Add project filtering by technology
⭐ Star this repo if you found it helpful!

Last Updated: November 2025
