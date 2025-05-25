# Connectify 🌐

A modern social media web application built with Django that allows users to connect, share moments, and discover new content. Connectify provides a clean and intuitive interface for social networking with features similar to popular platforms like Instagram.

## ✨ Features

### 🔐 User Authentication
- **User Registration & Login**: Secure user authentication system
- **Profile Management**: Customizable user profiles with bio, location, and profile pictures
- **Session Management**: Secure login/logout functionality

### 📸 Content Sharing
- **Photo Upload**: Share moments with image uploads
- **Captions**: Add descriptive captions to your posts
- **Timeline Feed**: View posts from users you follow in chronological order

### 🤝 Social Interactions
- **Follow/Unfollow**: Connect with other users
- **Like System**: Like and unlike posts
- **User Discovery**: Find and connect with new users through suggestions
- **Search Functionality**: Search for users by username

### 👤 Profile Features
- **Personal Profiles**: View user profiles with their posts, followers, and following count
- **Profile Customization**: Update profile picture, bio, and location
- **Post Gallery**: View all posts from a specific user

## 🛠️ Technology Stack

- **Backend**: Django 3.2.6
- **Database**: SQLite (development)
- **Frontend**: HTML, CSS, JavaScript
- **Authentication**: Django's built-in authentication system
- **File Handling**: Django's file upload system for images

## 📁 Project Structure

```
Connectify/
├── core/                   # Main application
│   ├── models.py          # Database models (Profile, Post, LikePost, FollowersCount)
│   ├── views.py           # Application logic and views
│   ├── urls.py            # URL routing
│   ├── admin.py           # Django admin configuration
│   └── migrations/        # Database migrations
├── social_book/           # Project configuration
│   ├── settings.py        # Django settings
│   ├── urls.py            # Main URL configuration
│   ├── wsgi.py            # WSGI configuration
│   └── asgi.py            # ASGI configuration
├── templates/             # HTML templates
│   ├── index.html         # Home feed
│   ├── profile.html       # User profiles
│   ├── search.html        # User search
│   ├── setting.html       # Profile settings
│   ├── signin.html        # Login page
│   └── signup.html        # Registration page
├── static/                # Static files (CSS, JS, images)
├── media/                 # User uploaded content
├── db.sqlite3            # SQLite database
└── manage.py             # Django management script
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Connectify
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install django==3.2.6
   pip install Pillow  # For image handling
   ```

4. **Apply database migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   Open your browser and navigate to `http://127.0.0.1:8000`

## 📱 Usage

### Getting Started
1. **Sign Up**: Create a new account using the registration form
2. **Complete Profile**: Add your profile picture, bio, and location
3. **Start Posting**: Upload your first photo with a caption
4. **Connect**: Search for users and start following them
5. **Engage**: Like posts and discover new content

### Key Pages
- **Home Feed** (`/`): View posts from users you follow
- **Profile** (`/profile/<username>`): View user profiles and their posts
- **Search** (`/search`): Find new users to follow
- **Settings** (`/settings`): Update your profile information
- **Upload** (`/upload`): Share new posts

## 🗄️ Database Models

### Profile
- User profile information including bio, profile image, and location
- One-to-one relationship with Django's User model

### Post
- User posts with images, captions, and timestamps
- UUID primary key for unique identification
- Like count tracking

### LikePost
- Tracks which users liked which posts
- Prevents duplicate likes from the same user

### FollowersCount
- Manages follower/following relationships
- Tracks social connections between users

## 🔧 Configuration

### Environment Variables
For production deployment, consider setting:
- `SECRET_KEY`: Django secret key
- `DEBUG`: Set to False for production
- `ALLOWED_HOSTS`: Configure allowed hosts
- `DATABASE_URL`: Production database configuration

### Media Files
- Profile images are stored in `media/profile_images/`
- Post images are stored in `media/post_images/`
- Default profile picture: `blank-profile-picture.png`

## 🚀 Deployment

### Production Considerations
1. **Security**: Update `SECRET_KEY` and set `DEBUG = False`
2. **Database**: Consider PostgreSQL for production
3. **Static Files**: Configure static file serving
4. **Media Files**: Set up proper media file handling
5. **HTTPS**: Enable SSL/TLS encryption

### Recommended Deployment Platforms
- **Heroku**: Easy deployment with PostgreSQL addon
- **DigitalOcean**: App Platform or Droplets
- **AWS**: EC2 with RDS
- **PythonAnywhere**: Simple Django hosting

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🐛 Known Issues & Future Enhancements

### Current Limitations
- Basic search functionality (username only)
- No real-time notifications
- Limited post types (images only)

### Planned Features
- [ ] Real-time messaging
- [ ] Story feature
- [ ] Video uploads
- [ ] Advanced search filters
- [ ] Email notifications
- [ ] Mobile responsive design improvements
- [ ] API endpoints for mobile app

## 📞 Support

If you encounter any issues or have questions:
1. Check the existing issues in the repository
2. Create a new issue with detailed description
3. Include steps to reproduce the problem

## 🙏 Acknowledgments

- Django community for the excellent framework
- Contributors and testers
- Open source community for inspiration

---

**Made with ❤️ using Django**
