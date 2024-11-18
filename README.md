# 💼 Job Post App

A modern Job Post App built with Vue.js to manage job postings. Perfect for learning Vue.js, Tailwind CSS, and full-stack development.

## ✨ Features

- View and manage job listings
- Create new job postings
- Update existing job details
- Delete outdated listings
- Real-time notifications
- Loading states for better UX

## 🛠️ Tech Stack

- Frontend: Vue.js 3
- Styling: Tailwind CSS
- Backend: JSON Server

## 📚 Tutorial Source

This project was built following the tutorial by:
- **Channel:** [Traversy Media](https://www.youtube.com/@TraversyMedia)
- **Video URL:** [Watch Tutorial](https://youtu.be/qZXt1Aom3Cs](https://youtu.be/VeNfHj6MhgA?si=IvHV0A9hjeLa2yGf )

## Getting Started

### Prerequisites
- Node.js
- npm

### Installation Steps

1. Clone the Repository
   ```bash
   git clone https://github.com/lahiruanushka/vue-job-listing-app.git
   cd vue-job-listing-app
   ```

2. Install Dependencies
   ```bash
   npm install
   ```

3. Run JSON Server
   ```bash
   npm run server
   ```

4. Start Development Server
   ```bash
   npm run dev
   ```

## 📁 Project Structure

```plaintext
job-post-app/
├── src/
│   ├── assets/            # Static assets
│   ├── components/        # Vue components
│   ├── pages/             # Page components
│   ├── jobs.json          # Mock data
│   ├── router/            # Vue Router setup
│   ├── App.vue           # Root component
│   ├── main.js           # Entry point
│   └── tailwind.config.js # Tailwind config
│
├── public/
├── package.json
└── README.md
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run server` - Start JSON server

## Dependencies

- Vue.js 3: Core framework
- Vue Router: Navigation
- Tailwind CSS: Styling
- Vue Toastification: Notifications
- Vue Spinner: Loading states
- Axios: API requests
- JSON Server: Mock backend

## Example Data Structure

```json
{
  "jobs": [
    {
      "title": "Senior Vue Developer",
      "type": "Full-Time",
      "location": "Boston, MA",
      "description": "We are seeking a talented Front-End Developer to join our team in Boston, MA. The ideal candidate will have strong skills in HTML, CSS, and JavaScript, with experience working with modern JavaScript frameworks such as Vue or Angular.",
      "salary": "$100K - $125K",
      "company": {
        "name": "NewTek Solutions teswf",
        "contactEmail": "contact@teksolutions.com",
        "contactPhone": "555-555-5555"
      },
      "id": "1"
    },
    {
      "id": "3",
      "title": "Vue.js Developer",
      "type": "Full-Time",
      "description": "Are you passionate about front-end development? Join our team in vibrant Brooklyn, NY, and work on exciting projects that make a difference. We offer competitive compensation and a collaborative work environment where your ideas are valued.",
      "location": "Brooklyn, NY",
      "salary": "$70K - $80K",
      "company": {
        "name": "Dolor Cloud",
        "description": "Dolor Cloud is a leading technology company specializing in digital solutions for businesses of all sizes. With a focus on innovation and customer satisfaction, we are committed to delivering cutting-edge products and services.",
        "contactEmail": "contact@dolorsitamet.com",
        "contactPhone": "555-555-5555"
      }
    },
]
}
```

## 📸 Screenshots

### Home Page
The home view of the app.

![Job Listings](/screenshots/home.png)

### Job Listings View
The main dashboard where all job postings are displayed.

![Job Listings](/screenshots/job-listings.png)

### Add Job Form
User-friendly form for creating job posts.

![Job Form](/screenshots/add-job-form.png)

### Edit Job Form
User-friendly form for updating job posts.

![Job Form](/screenshots/edit-job-form.png)

## Learning Objectives

- Master Vue.js component creation
- Learn Tailwind CSS styling
- Implement CRUD operations
- Handle API integrations
- Build responsive UIs


## 🚀 Future Improvements

- Search functionality
- User authentication
- Advanced filtering
- Real database integration
