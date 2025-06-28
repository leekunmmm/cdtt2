# IT Job Search Web Application

A comprehensive web application for IT professionals to search for jobs, manage their profiles, connect with IT companies, and read industry-related blog posts.

## 🚀 Features

### Core Features
- **User Authentication & Management** - Secure registration, login, and profile management
- **Job Search & Filtering** - Advanced job search with multiple filters
- **Company Profiles** - Detailed company information and job listings
- **Blog System** - IT industry blog with articles, tags, and comments
- **Resume Management** - CV templates and upload functionality
- **Social Authentication** - Login with Google, GitHub, etc.

### Blog System Features
- **Blog Posts** - Rich content with images, tags, and summaries
- **Categories & Tags** - Organized content with tag-based filtering
- **Comments System** - User interaction and discussions
- **SEO Optimized** - Slug-based URLs for better SEO
- **Responsive Design** - Mobile-friendly blog interface

## 🛠 Tech Stack

### Backend
- **Django 5.0.2** - Web framework
- **Django REST Framework** - API development
- **PostgreSQL** - Database (with SQLite for development)
- **JWT Authentication** - Secure token-based auth
- **Pillow** - Image processing
- **Social Auth** - OAuth integration

### Frontend
- **HTML/CSS/JavaScript** - Traditional web stack
- **Bootstrap/Material-UI** - UI components
- **Responsive Design** - Mobile-first approach

### Development Tools
- **Git** - Version control
- **Virtual Environment** - Python dependency isolation
- **Gunicorn** - Production server

## 📁 Project Structure

```
KevinITJob/
├── backend/                    # Django backend
│   ├── blog_posts/            # Blog application
│   │   ├── models.py          # Blog models (Blog, Comment, BlogPost)
│   │   ├── views.py           # Blog views (list, detail)
│   │   ├── urls.py            # Blog URL routing
│   │   └── management/        # Custom commands
│   ├── it_job_search/         # Main Django project
│   │   ├── templates/         # HTML templates
│   │   │   ├── blog_list.html # Blog listing page
│   │   │   └── blog_detail.html # Blog detail page
│   │   └── urls.py            # Main URL configuration
│   ├── job_listings/          # Job management app
│   ├── company_profiles/      # Company management app
│   ├── user_management/       # User management app
│   └── media/                 # Uploaded files
│       └── blog_images/       # Blog post images
├── frontend/                  # Frontend assets
│   └── img/                   # Static images
├── venv/                      # Python virtual environment
├── requirements.txt           # Python dependencies
├── .gitignore                # Git ignore rules
└── README.md                 # Project documentation
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Node.js (for frontend development)
- Git

### Backend Setup

1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd KevinITJob
   ```

2. **Create and activate virtual environment:**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Navigate to backend and run migrations:**
   ```bash
   cd backend
   python manage.py migrate
   ```

5. **Seed sample data:**
   ```bash
   python manage.py seed_blogposts
   python manage.py seed_jobs
   ```

6. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

7. **Access the application:**
   - Main site: http://localhost:8000
   - Blog: http://localhost:8000/blog/
   - Admin: http://localhost:8000/admin/

### Frontend Setup (Optional)

1. **Install Node.js dependencies:**
   ```bash
   cd frontend
   npm install
   ```

2. **Run frontend development server:**
   ```bash
   npm start
   ```

## 📝 Blog System Usage

### Creating Blog Posts
1. Access Django admin at `/admin/`
2. Navigate to "Blog posts" section
3. Add new blog post with:
   - Title
   - Summary
   - Content (HTML supported)
   - Image (optional)
   - Tags (comma-separated)

### Blog Features
- **Automatic Slug Generation** - URLs are automatically created from titles
- **Tag System** - Organize posts with tags
- **Image Support** - Upload and display images
- **Related Posts** - Show related articles on detail pages
- **Responsive Design** - Works on all devices

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the backend directory:
```env
SECRET_KEY=your-secret-key
DEBUG=True
DATABASE_URL=sqlite:///db.sqlite3
ALLOWED_HOSTS=localhost,127.0.0.1
```

### Database Configuration
The project uses SQLite by default for development. For production, configure PostgreSQL in `settings.py`.

## 🚀 Deployment

### Production Setup
1. Set `DEBUG=False` in settings
2. Configure production database
3. Set up static file serving
4. Use Gunicorn as WSGI server
5. Configure reverse proxy (Nginx)

### Docker Deployment (Optional)
```bash
docker-compose up -d
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes
4. Commit your changes: `git commit -m 'Add feature'`
5. Push to the branch: `git push origin feature-name`
6. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue on GitHub
- Contact the development team
- Check the documentation

## 🔄 Version History

- **v1.0.0** - Initial release with basic job search and blog functionality
- **v1.1.0** - Added user authentication and company profiles
- **v1.2.0** - Enhanced blog system with comments and tags 