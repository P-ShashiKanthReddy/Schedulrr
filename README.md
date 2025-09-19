# Schedulrr - Modern Scheduling Application

A comprehensive scheduling platform built with Next.js, React, and modern web technologies. Schedulrr simplifies appointment booking and calendar management for professionals and businesses.

## 🚀 Features

- **User Authentication**: Secure authentication powered by Clerk
- **Event Management**: Create, edit, and delete custom event types
- **Availability Management**: Set your working hours and availability preferences
- **Smart Scheduling**: Intelligent booking system that prevents conflicts
- **Google Calendar Integration**: Seamless synchronization with Google Calendar
- **Meeting Links**: Automatic Google Meet link generation for bookings
- **Responsive Design**: Mobile-first design that works on all devices
- **Real-time Updates**: Live updates for bookings and availability
- **Time Zone Support**: Automatic time zone handling for global users
- **Email Notifications**: Automated booking confirmations and reminders

## 🛠️ Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **React 18** - UI library with hooks and modern patterns
- **Tailwind CSS** - Utility-first CSS framework
- **Shadcn/ui** - Modern UI component library
- **React Hook Form** - Form handling and validation
- **Zod** - Schema validation
- **Lucide React** - Beautiful icons

### Backend & Database
- **Prisma** - Modern database toolkit and ORM
- **PostgreSQL** - Robust relational database
- **Server Actions** - Next.js server-side functions

### Authentication & APIs
- **Clerk** - Complete authentication solution
- **Google APIs** - Calendar and Meet integration
- **Google OAuth** - Secure API access

### Development Tools
- **ESLint** - Code linting and formatting
- **PostCSS** - CSS processing
- **React Spinners** - Loading indicators

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd schedulrr
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   ```env
   # Database
   DATABASE_URL="your-postgresql-connection-string"

   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your-clerk-publishable-key"
   CLERK_SECRET_KEY="your-clerk-secret-key"
   NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
   NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL="/dashboard"
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL="/dashboard"

   # Google OAuth (for Calendar integration)
   GOOGLE_CLIENT_ID="your-google-client-id"
   GOOGLE_CLIENT_SECRET="your-google-client-secret"
   ```

4. **Set up the database**
   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Project Structure

```
schedulrr/
├── app/                    # Next.js App Router
│   ├── (auth)/            # Authentication pages
│   ├── (main)/            # Main application pages
│   │   ├── dashboard/     # User dashboard
│   │   ├── events/        # Event management
│   │   ├── meetings/      # Meeting management
│   │   └── availability/  # Availability settings
│   ├── [username]/        # Public user profiles
│   └── globals.css        # Global styles
├── actions/               # Server actions
├── components/            # Reusable React components
│   └── ui/               # UI component library
├── hooks/                 # Custom React hooks
├── lib/                   # Utility functions and configurations
├── prisma/               # Database schema and migrations
└── public/               # Static assets
```

## 🔧 Configuration

### Database Setup
The application uses PostgreSQL with Prisma ORM. The database schema includes:
- **Users**: User profiles and authentication data
- **Events**: Event types and configurations
- **Bookings**: Scheduled appointments
- **Availability**: User availability settings

### Authentication Setup
Clerk handles all authentication flows including:
- Sign up/Sign in
- User profile management
- OAuth integrations
- Session management

### Google Integration
To enable Google Calendar integration:
1. Create a Google Cloud Project
2. Enable Calendar API and Google Meet API
3. Configure OAuth consent screen
4. Add your domain to authorized origins
5. Update environment variables with your credentials

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your repository to Vercel
2. Add environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Other Platforms
The application can be deployed on any platform that supports Next.js:
- Netlify
- Railway
- DigitalOcean App Platform
- AWS Amplify

## 📱 Usage

### For Event Hosts
1. **Sign up** and complete your profile
2. **Set availability** by defining your working hours
3. **Create events** with custom durations and descriptions
4. **Share your booking link** with clients or colleagues
5. **Manage bookings** from your dashboard

### For Clients
1. **Visit the host's booking page**
2. **Select an event type**
3. **Choose available time slot**
4. **Fill in booking details**
5. **Receive confirmation** with meeting link

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow the existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [Clerk](https://clerk.dev/) for authentication services
- [Prisma](https://prisma.io/) for database management
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Shadcn/ui](https://ui.shadcn.com/) for UI components

## 📞 Support

If you have any questions or need help:
- Open an issue on GitHub
- Check the documentation
- Contact the development team

## 🔮 Roadmap

- [ ] Mobile app development
- [ ] Advanced analytics dashboard
- [ ] Team scheduling features
- [ ] Integration with more calendar providers
- [ ] Automated reminder system
- [ ] Payment integration
- [ ] Multi-language support
- [ ] Advanced customization options

---

**Made with ❤️ by Shashikanth**