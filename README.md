# Startup Builder Mode - Setup Guide

## Quick Start

### Option 1: Import via Bob Settings (Recommended)

1. **Open Bob Settings**
   - Click the Bob icon in VS Code
   - Go to Settings → Custom Modes

2. **Add the Mode**
   - Click "Add Custom Mode"
   - Download the file: https://github.com/ijgitsh/ibm-bob-startup-builder/blob/main/startup-builder-mode.yaml
   - Select the file: `startup-builder-mode.yaml`
   - Bob will automatically load the mode

3. **Activate the Mode**
   - Open a new chat with Bob
   - Type: `/mode startup-builder`
   - Or let Bob auto-select it when you say "Build me a startup for..."

### Option 2: Manual Installation

1. **Copy the Mode File**
   ```bash
   cp presaledemoBuilder/startup-builder-mode.yaml ~/.bob/modes/
   ```

2. **Restart VS Code**
   - Bob will automatically detect the new mode

3. **Verify Installation**
   - Open Bob
   - Type: `/modes` to see all available modes
   - You should see "🚀 Startup Builder" in the list

## How to Use

### Basic Usage

Simply tell Bob what you want to build:

```
Build me a startup for a freelance marketplace where designers can showcase 
portfolios and clients can post projects
```

Bob will:
1. Ask clarifying questions about features and tech preferences
2. Generate the complete project structure
3. Create all code files (frontend, backend, database)
4. Provide setup instructions
5. Give you a one-command startup script

### Example Prompts

**Simple**:
```
Build me a SaaS analytics dashboard
```

**Detailed**:
```
Create an MVP for an online course platform with:
- Video lessons and live classes
- Student and instructor roles
- Payment integration with Stripe
- Certificate generation
- Mobile-responsive design
```

**With Tech Preferences**:
```
Build a task management app using React and FastAPI with real-time 
collaboration features
```

### After Generation

1. **Navigate to the project**:
   ```bash
   cd startup-{your-project-name}
   ```

2. **Start the development servers**:
   ```bash
   ./scripts/dev.sh
   ```

3. **Open in browser**:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000
   - API Docs: http://localhost:8000/docs

4. **Make changes**:
   ```
   Add a feature for user notifications
   Change the color scheme to dark mode
   Integrate with SendGrid for emails
   ```

## What Gets Generated

Every startup project includes:

### Frontend (React + Vite + Tailwind)
- ✅ Responsive UI components
- ✅ User authentication pages
- ✅ Dashboard and main features
- ✅ API integration
- ✅ Loading and error states
- ✅ Accessible (WCAG 2.1 AA)

### Backend (FastAPI + PostgreSQL)
- ✅ RESTful API endpoints
- ✅ JWT authentication
- ✅ Database models and migrations
- ✅ Input validation
- ✅ Auto-generated API docs
- ✅ Error handling

### Database
- ✅ PostgreSQL schema
- ✅ Migrations (Alembic)
- ✅ Seed data for testing
- ✅ Indexes and constraints

### DevOps
- ✅ Docker Compose setup
- ✅ Environment configuration
- ✅ Setup and deployment scripts
- ✅ Git repository with .gitignore

### Documentation
- ✅ README with setup guide
- ✅ ARCHITECTURE with system design
- ✅ API documentation
- ✅ Deployment instructions

## Features Included

### Always Included
- User authentication (sign up, sign in, password reset)
- Role-based access control
- Responsive mobile-first UI
- RESTful API with validation
- Database with migrations
- Docker development environment
- Comprehensive documentation

### Optional (Based on Your Idea)
- Payment processing (Stripe)
- File uploads (S3/local)
- Real-time features (WebSockets)
- Email notifications (SendGrid)
- Search functionality
- Social authentication (OAuth)
- Background jobs (Celery)
- Caching (Redis)
- Analytics tracking

## Tech Stack

### Default Stack
- **Frontend**: React 18, Vite, Tailwind CSS
- **Backend**: FastAPI (Python), SQLAlchemy
- **Database**: PostgreSQL
- **Auth**: JWT tokens
- **Deployment**: Docker Compose

### Alternative Options
Bob can use different technologies if you specify:
- **Frontend**: Vue, Svelte, Next.js
- **Backend**: Express (Node.js), NestJS, Django
- **Database**: MongoDB, MySQL, SQLite
- **UI**: Material-UI, Chakra UI, Carbon Design

## Tips for Best Results

1. **Be Specific**: More detail = better output
   - ❌ "Build a social network"
   - ✅ "Build a social network for book lovers with reading lists, reviews, and book clubs"

2. **Define User Roles**: Specify who uses the app
   - "Users can be readers or authors. Authors can publish, readers can review."

3. **List Key Features**: Enumerate must-haves
   - "Must have: profiles, search, notifications. Nice to have: recommendations."

4. **Mention Integrations**: Call out third-party services
   - "Integrate with Stripe for payments and SendGrid for emails"

5. **Specify Constraints**: Technical requirements
   - "Must work offline, mobile-first, GDPR compliant"

## Troubleshooting

### Mode Not Showing Up
- Restart VS Code
- Check the YAML file is valid (no syntax errors)
- Verify the file is in the correct location

### Build Fails
- Ensure you have Node.js and Python installed
- Check Docker is running (for database)
- Review the error message and ask Bob to fix it

### Can't Start the App
- Run `./scripts/setup.sh` first
- Check `.env` file has correct values
- Ensure ports 3000 and 8000 are available

## Next Steps

After Bob generates your startup:

1. **Review the Code**: Understand the architecture
2. **Customize**: Adjust branding, colors, copy
3. **Test**: Run through user flows
4. **Deploy**: Use the deployment guide
5. **Iterate**: Add features, improve UX
6. **Launch**: Share with users!

## Support

If you encounter issues:
1. Ask Bob to fix the problem: "Fix the error where..."
2. Check the generated README.md for troubleshooting
3. Review the ARCHITECTURE.md for system design

## Examples

### Example 1: Freelance Marketplace
```
Build me a marketplace for freelance designers where clients can post 
projects, designers submit proposals, with portfolios, ratings, and chat
```

**Result**: Complete marketplace with user roles, project management, proposal system, portfolio showcases, rating/review system, real-time messaging, and payment integration.

### Example 2: SaaS Analytics
```
Create a SaaS analytics dashboard for e-commerce stores to track sales, 
customer behavior, and inventory
```

**Result**: Multi-tenant SaaS with store integrations, real-time metrics, custom reports, alerts, team collaboration, and data export.

### Example 3: Learning Platform
```
Build an online course platform with video lessons, live classes, 
assignments, and certificates
```

**Result**: Full learning management system with course creation, video hosting, live streaming, assignment submission, grading, and certificate generation.

## License

The generated code is yours to use, modify, and deploy as you wish. No attribution required.

---

**Ready to build your startup?** Just tell Bob your idea! 🚀
