Welcome to CarMagazine, a high-performance Drupal 11 application designed for automotive journalism, vehicle reviews, and industry news.

## Project Overview

CarMagazine is built on Drupal 11, leveraging the latest features in core for improved performance, a streamlined administrative experience, and modern decoupled capabilities. This project serves as a digital hub for automotive enthusiasts, featuring structured content for vehicle specifications, high-resolution galleries, and expert editorials.

## Technical Stack

Core: Drupal 11.x

PHP: 8.3+ (Required)

Database: MySQL 8.0+ / MariaDB 10.6+ / PostgreSQL 16+

Frontend: SDC (Single Directory Components) & Tailwind CSS

Local Development: DDEV (Recommended) or Lando

## Installation

### 1. Prerequisites

Ensure you have Composer and a local PHP environment installed. We recommend using DDEV for a seamless setup.

### 2. Clone the Repository

Bash
git clone https://github.com/your-org/carmagazine.git
cd carmagazine

### 3. Setup with DDEV

Bash
ddev config
ddev start
ddev composer install

### 4. Install Drupal

Use Drush to install the site with the minimal or standard profile:

Bash
ddev drush site:install --db-url=mysql://db:db@db/db -y

## Key Features

Automotive Content Types: Pre-configured schemas for Vehicle Reviews, Manufacturer News, and Buyer Guides.

Advanced Media Management: Optimized for large-scale image assets and embedded video content using Drupal's Media Library.

Taxonomy Architecture: Deeply nested categories for Make, Model, Engine Type (EV, Hybrid, ICE), and Year.

SEO Optimized: Out-of-the-box configuration for Pathauto, Metatag, and Simple XML Sitemap.

## Development Workflow

### Compiling Assets

This project uses Vite for frontend asset orchestration.

Bash
npm install
npm run dev # For local development
npm run build # For production-ready assets

### Running Updates

When pulling new changes, always sync your configuration and database:

Bash
ddev composer install
ddev drush updb -y
ddev drush cim -y
ddev drush cr

## Configuration Management

All site configurations are stored in the ../config/sync directory.

Export: drush cex

Import: drush cim

## Contributing

Create a new feature branch: git checkout -b feature/issue-id-description

Commit your changes following the Drupal coding standards.

Ensure all tests pass: ddev drush test-run

Open a Pull Request against the develop branch.

## License

This project is open-source software licensed under the GPL-2.0-or-later.
