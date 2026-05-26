# Developer Portfolio

A modern, fully responsive personal developer portfolio website with a working contact form that sends emails directly to your inbox.

## Features

✨ **Complete Portfolio Website**
- Name and professional tagline
- Featured projects section with project cards
- Comprehensive skills section organized by category
- LinkedIn profile link
- Smooth scrolling navigation

📧 **Working Contact Form**
- Contact form with validation
- Email notifications sent to your inbox
- Automatic confirmation emails to visitors
- Form error handling and user feedback

🎨 **Modern Design**
- Responsive design (mobile, tablet, desktop)
- Gradient color scheme
- Smooth animations and transitions
- Interactive hover effects
- Professional typography

🚀 **Easy to Deploy**
- Node.js/Express backend
- Nodemailer for email sending
- Environment-based configuration
- Ready for deployment on Heroku, Railway, or any Node.js hosting

## Project Structure

```
.
├── index.html          # Main HTML file
├── styles.css          # CSS styles and responsive design
├── script.js           # Frontend JavaScript functionality
├── server.js           # Node.js/Express backend server
├── package.json        # Project dependencies
├── .env.example        # Environment variables template
├── .gitignore          # Git ignore configuration
└── README.md           # This file
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Gmail account (or another email service)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/ashwika0422/first.git
cd first
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment variables**
```bash
cp .env.example .env
```

Then edit `.env` with your email configuration:
```
EMAIL_SERVICE=gmail
EMAIL_USER=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
PORT=3000
```

### Gmail Setup

If using Gmail, follow these steps:

1. Enable 2-Step Verification on your Google Account
2. Generate an [App Password](https://myaccount.google.com/apppasswords)
3. Use the generated app password in your `.env` file

### Running Locally

```bash
# Development mode (with auto-reload)
npm run dev

# Production mode
npm start
```

Visit `http://localhost:3000` in your browser.

## Customization

### Update Portfolio Information

Edit `index.html` to customize:

- **Name & Tagline**: Update in the Hero section
- **Projects**: Modify the projects section
- **Skills**: Add or remove skills in the skills section
- **Contact Info**: Update email, phone, and location
- **Social Links**: Update LinkedIn, GitHub, and Twitter URLs

### Update Styling

Modify `styles.css` to customize:

- **Colors**: Change CSS custom properties in `:root` section
- **Typography**: Adjust font sizes and weights
- **Layout**: Modify grid templates and spacing

## Email Configuration

### Using Different Email Services

The contact form can work with various email services:

**Gmail** (Recommended)
- Use App Passwords (recommended)
- Or enable "Less secure app access"

**Outlook/Hotmail**
```env
EMAIL_SERVICE=hotmail
```

## Deployment

### Deploy to Heroku

```bash
# Install Heroku CLI and login
heroku login

# Create new app
heroku create your-app-name

# Set environment variables
heroku config:set EMAIL_USER=your-email@gmail.com
heroku config:set EMAIL_PASSWORD=your-app-password

# Deploy
git push heroku main
```

### Deploy to Railway

1. Push your code to GitHub
2. Connect your GitHub repository to Railway
3. Add environment variables in Railway dashboard
4. Deploy

## API Endpoints

### POST `/api/send-email`

Sends an email from the contact form.

**Request Body:**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "subject": "Project Inquiry",
  "message": "Hi, I'm interested in your services..."
}
```

**Success Response (200):**
```json
{
  "success": "Email sent successfully"
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Troubleshooting

### Emails not sending

1. **Check credentials**: Verify EMAIL_USER and EMAIL_PASSWORD in `.env`
2. **Gmail**: Ensure you're using an App Password, not your regular password
3. **SMTP errors**: Check your email service SMTP settings

### Form not submitting

1. Open browser console (F12) for error messages
2. Check that the server is running on the correct port
3. Verify CORS is enabled

### Styling issues

1. Hard refresh the page (Ctrl+F5 or Cmd+Shift+R)
2. Clear browser cache
3. Check that `styles.css` is being loaded

## License

MIT License - feel free to use this for your own portfolio

## Support

If you encounter issues, check the troubleshooting section or open an issue on GitHub.

---

**Happy Coding!** 🚀
