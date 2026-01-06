# Gestion Outils Leveilleford - Inventory Management System

A comprehensive web-based inventory management system built with CodeIgniter, PHP, and MySQL. This system provides complete stock management capabilities including product cataloging, order processing, user management, and sales reporting.

## 🚀 Features

### Core Functionality
- **User Management** - Create, view, update, and delete user accounts with role-based access control
- **Group & Permissions** - Flexible permission system with user groups and granular access controls
- **Product Catalog** - Complete product management with attributes, brands, and categories
- **Order Management** - Track and manage customer orders with detailed item tracking
- **Inventory Control** - Monitor stock levels across multiple stores/locations
- **Sales Reporting** - Visualize sales data with interactive charts and yearly reports
- **Company Settings** - Configure company information, VAT, service charges, and branding

### Additional Features
- Responsive AdminLTE dashboard interface
- Rich text editing with CKEditor
- Interactive data visualization (Chart.js, Morris.js)
- Multi-store support
- Product attributes (color, size, etc.)
- Brand and category management
- User activity tracking
- Secure authentication and session management

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| **Backend Framework** | CodeIgniter (PHP MVC Framework) |
| **Language** | PHP 5.6+ |
| **Database** | MySQL / Azure MySQL Database |
| **Frontend** | AdminLTE (Bootstrap-based) |
| **JavaScript Libraries** | jQuery, Chart.js, Morris.js, Moment.js |
| **Text Editor** | CKEditor |
| **UI Components** | Bootstrap, Select2, Fullcalendar |
| **Deployment** | Azure App Service |
| **CI/CD** | GitHub Actions |

## 📋 System Requirements

### Server Requirements
- **PHP Version:** 5.6 or newer (supports 5.3.7+, but 5.6+ recommended for security)
- **Web Server:** Apache with mod_rewrite enabled
- **Database:** MySQL 5.6+ or MariaDB 10.0+
- **PHP Extensions:**
  - mysqli
  - mbstring
  - openssl
  - xml
  - json

### Recommended Development Environment
Choose one of the following:
- **XAMPP** (Cross-platform)
- **MAMP** (macOS)
- **LAMP** (Linux)
- **WAMP** (Windows)

## 📦 Installation

### Local Development Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/cadieuxj/Gestionoutilsleveilleford.git
   cd Gestionoutilsleveilleford
   ```

2. **Set Up Web Server**
   - Move the project to your web server's root directory:
     - XAMPP: `C:\xampp\htdocs\Gestionoutilsleveilleford\`
     - MAMP: `/Applications/MAMP/htdocs/Gestionoutilsleveilleford/`
     - LAMP: `/var/www/html/Gestionoutilsleveilleford/`

3. **Create Database**
   - Open phpMyAdmin (usually at `http://localhost/phpmyadmin`)
   - Create a new database named `stock`
   - Import the SQL schema: Click "Import" and select `stock.sql` from the project root

4. **Configure Database Connection**
   Edit `application/config/database.php`:
   ```php
   $db['default'] = array(
       'hostname' => 'localhost',
       'username' => 'root',
       'password' => '',
       'database' => 'stock',
       // ... other settings
   );
   ```

5. **Configure Base URL**
   Edit `application/config/config.php`:
   ```php
   $config['base_url'] = 'http://localhost/Gestionoutilsleveilleford/';
   ```

6. **Start Services**
   - Start Apache and MySQL from your application server control panel
   - Access the application at: `http://localhost/Gestionoutilsleveilleford/`

### Azure Deployment

The project is configured for Azure App Service deployment:

1. **Database Setup**
   - Azure MySQL Database is pre-configured in `application/config/database.php`
   - Database server: `gestionoutilsleveilleford-server.mysql.database.azure.com`

2. **Automated Deployment**
   - Push to the designated branch triggers GitHub Actions workflow
   - Azure App Service automatically deploys the application
   - Workflow file: `.github/workflows/main_gestionoutilsleveilleford.yml`

## 🔐 Default Credentials

**Super Admin Account:**
- **Email:** admin@admin.com
- **Password:** password

**⚠️ Important:** Change these credentials immediately after first login!

## 🗄️ Database Schema

The system uses 12 main tables:

| Table | Purpose |
|-------|---------|
| `users` | User account information |
| `user_group` | User-to-group relationships |
| `groups` | Permission groups and roles |
| `products` | Product catalog |
| `brands` | Product brands |
| `categories` | Product categories |
| `attributes` | Product attributes (color, size, etc.) |
| `attribute_value` | Attribute value options |
| `orders` | Customer orders |
| `orders_item` | Order line items |
| `stores` | Store/location information |
| `company` | Company settings and configuration |

## 📸 Screenshots

![Login Page](https://github.com/ronknight/InventorySystem/blob/master/assets/images/screenshots/login.PNG)
![Dashboard](https://github.com/ronknight/InventorySystem/blob/master/assets/images/screenshots/dashboard.PNG)
![Database](https://github.com/ronknight/InventorySystem/blob/master/assets/images/screenshots/database.PNG)

## 🎯 Usage Guide

### First-Time Setup
1. Log in with default admin credentials
2. Navigate to **Company** settings and update company information
3. Create user groups with appropriate permissions
4. Add brands and categories for your products
5. Create store/location records
6. Add products to the catalog
7. Create additional user accounts and assign to groups

### Daily Operations
- **Dashboard** - View key metrics (total products, orders, users, stores)
- **Products** - Add/edit products with attributes and pricing
- **Orders** - Create and track customer orders
- **Reports** - View sales analytics and generate reports
- **Stores** - Manage inventory across multiple locations

## 🔧 Configuration

### Important Configuration Files

| File | Purpose |
|------|---------|
| `application/config/config.php` | Base URL, encryption, session settings |
| `application/config/database.php` | Database connection parameters |
| `application/config/routes.php` | URL routing configuration |
| `application/config/autoload.php` | Auto-loaded libraries and helpers |

### Customization
- **Company Logo:** Upload via Company settings in the application
- **Theme:** Modify `assets/dist/` files for custom styling
- **Permissions:** Configure group permissions through the Groups interface

## 🤝 Contributing

Contributions are welcome! Please read [contributing.md](contributing.md) for details on the code of conduct and the process for submitting pull requests.

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Original Source:** [CodeFolder](https://codersfolder.com/2018/02/stock-management-system-v2-codeigniter/) - Stock Management System v2
- **Framework:** [CodeIgniter](https://codeigniter.com/) - PHP Web Framework
- **Theme:** [AdminLTE](https://adminlte.io/) - Bootstrap Admin Dashboard Template
- **UI Components:** Bootstrap, jQuery, Chart.js, CKEditor, and various open-source libraries

## 📞 Support

For issues, questions, or contributions:
- Open an issue in the GitHub repository
- Check existing documentation and issues before posting

## 🔄 Version History

- **v2.0** - Enhanced Azure deployment support
- **v1.0** - Initial release based on CodeFolder inventory system

---

**Built with ❤️ for efficient inventory management**
