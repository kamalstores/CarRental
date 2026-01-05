# 🚗 CarRental

A full-stack car rental platform that connects car owners with renters. Built with React, Node.js, Express, and MongoDB.


## 📋 Overview

CarRental is a modern web application that enables users to browse, search, and book rental cars while allowing car owners to list their vehicles and manage bookings. The platform features a clean, responsive interface with separate dashboards for renters and car owners. 

## ✨ Features

### For Renters
- 🔍 **Search & Filter**: Search cars by brand, model, location, and availability
- 📅 **Date-based Booking**: Select pickup and return dates to check availability
- 💳 **Easy Reservations**: Book cars without credit card requirements
- 📱 **Responsive Design**:  Seamless experience across all devices
- 📊 **My Bookings**: View and manage your rental history

### For Car Owners
- ➕ **List Your Car**: Add vehicles with detailed specifications
- 🖼️ **Image Upload**: Upload car images via ImageKit integration
- 📈 **Dashboard**: Track bookings and earnings
- 🚙 **Manage Cars**: Update or remove your listed vehicles
- 📋 **Booking Management**: View and manage customer bookings

### Car Details
- Vehicle specifications (brand, model, year)
- Transmission type (Manual/Automatic/Semi-Automatic)
- Fuel type (Gas, Diesel, Petrol, Electric, Hybrid)
- Seating capacity
- Category (SUV, Sedan, etc.)
- Daily pricing
- Location
- Availability status
- Features (360° Camera, Bluetooth, GPS, Heated Seats, etc.)

## 🛠️ Tech Stack

### Frontend
- **React 19.1.1** - UI framework
- **React Router DOM** - Navigation
- **Vite** - Build tool and dev server
- **Tailwind CSS 4.1.16** - Styling
- **Motion** - Animations
- **Axios** - HTTP client
- **React Hot Toast** - Notifications

### Backend
- **Node.js** - Runtime environment
- **Express 5.1.0** - Web framework
- **MongoDB** with **Mongoose 8.19.2** - Database
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **ImageKit** - Image storage and optimization
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing

## 📁 Project Structure

```
CarRental/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── assets/        # Images and static files
│   │   ├── components/    # Reusable components
│   │   ├── context/       # React Context (AppContext)
│   │   ├── pages/         # Page components
│   │   │   ├── owner/     # Owner dashboard pages
│   │   │   ├── Cars.jsx
│   │   │   ├── CarDetails.jsx
│   │   │   └── MyBookings.jsx
│   │   └── App.jsx        # Main app component
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
│
└── server/                # Backend Node. js application
    ├── configs/           # Configuration files (DB)
    ├── controllers/       # Route controllers
    ├── middleware/        # Custom middleware
    ├── models/            # Mongoose models
    │   └── Car.js
    ├── routes/            # API routes
    │   ├── userRoutes.js
    │   ├── ownerRoutes.js
    │   └── bookingRoutes.js
    ├── server.js          # Entry point
    └── package.json
```

## 🚀 Getting Started

### Prerequisites
- Node. js (v14 or higher)
- MongoDB database
- ImageKit account (for image uploads)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/kamalstores/CarRental. git
   cd CarRental
   ```

2. **Setup Backend**
   ```bash
   cd server
   npm install
   ```

   Create a `.env` file in the server directory:
   ```env
   PORT=3000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
   IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
   IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint
   ```

   Start the server:
   ```bash
   npm run server    # Development with nodemon
   npm start         # Production
   ```

3. **Setup Frontend**
   ```bash
   cd ../client
   npm install
   ```

   Create a `.env` file in the client directory:
   ```env
   VITE_BASE_URL=http://localhost:3000
   VITE_CURRENCY=$
   ```

   Start the development server:
   ```bash
   npm run dev
   ```

4. **Access the application**
   - Frontend: `http://localhost:5173`
   - Backend: `http://localhost:3000`

## 🔌 API Endpoints

### User Routes (`/api/users`)
- Authentication and user management

### Owner Routes (`/api/owner`)
- `POST /add-car` - List a new car
- Car management operations

### Booking Routes (`/api/bookings`)
- `POST /create` - Create a new booking
- Booking management operations

## 🎨 Key Components

### Frontend Components
- `Hero` - Landing page hero section with search
- `CarCard` - Individual car display card
- `FeaturedSection` - Featured cars showcase
- `Banner` - Call-to-action for car owners
- `Navbar` & `Footer` - Navigation and footer
- `Loader` - Loading state component

### Pages
- `Home` - Landing page
- `Cars` - Browse all available cars
- `CarDetails` - Individual car details and booking
- `MyBookings` - User's rental history
- `Owner/Dashboard` - Owner analytics
- `Owner/AddCar` - List new vehicle
- `Owner/ManageCars` - Update/delete cars
- `Owner/ManageBookings` - Handle bookings

## 🔐 Authentication

The application uses JWT (JSON Web Tokens) for secure authentication:
- Token-based authentication
- Protected routes for owners
- Secure password hashing with bcrypt

## 📱 Responsive Design

The application is fully responsive and optimized for: 
- Desktop (1920px and above)
- Laptop (1024px - 1919px)
- Tablet (768px - 1023px)
- Mobile (320px - 767px)

## 🌟 Features in Detail

### Search Functionality
Users can search for cars by:
- Brand name
- Model
- Location
- Pickup/Return dates
- Availability

### Booking System
- Date validation
- Availability checking
- Price calculation based on rental duration
- Booking confirmation with toast notifications

### Car Management
Owners can:
- Upload car images
- Set daily rental rates
- Mark cars as available/unavailable
- Update car details
- View booking statistics

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**kamalstores**
- GitHub: [@kamalstores](https://github.com/kamalstores)

## 🙏 Acknowledgments

- React team for the amazing framework
- Tailwind CSS for the utility-first CSS framework
- ImageKit for image optimization
- MongoDB for the database solution

## 📞 Support

For support, please open an issue in the GitHub repository.

---

Made with ❤️ by kamalstores
