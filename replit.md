# Overview

This is a Digital Platform for Centralized Alumni Data Management and Engagement built for a hackathon. The application is designed to connect and facilitate engagement among GGSIPU (Guru Gobind Singh Indraprastha University) alumni. The platform features a clean, minimal design with white as the primary background color and teal as the complementary accent color.

The application allows students to register with their university details and browse through a comprehensive alumni directory with search and filtering capabilities. Alumni profiles display essential information including name, college, batch year, designation, and current company, enabling networking and professional connections within the university community.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture

The frontend is built using React with TypeScript, utilizing a modern component-based architecture. The application uses Vite as the build tool for fast development and optimized production builds. The UI is constructed with shadcn/ui components built on top of Radix UI primitives, providing accessible and customizable interface elements.

State management is handled through React Query (TanStack Query) for server state management, providing efficient data fetching, caching, and synchronization. The application uses Wouter for client-side routing, offering a lightweight alternative to React Router. Form handling is implemented using React Hook Form with Zod schema validation for type-safe form processing.

The styling system is built on Tailwind CSS with a custom design system using CSS custom properties for consistent theming. The application supports both light and dark modes through CSS variable-based color schemes.

## Backend Architecture

The backend follows a REST API architecture built with Express.js and TypeScript. The server implements a clean separation of concerns with dedicated modules for routing, storage, and middleware. The application uses an in-memory storage implementation that loads alumni data from a JSON file, making it suitable for prototyping and demonstration purposes.

The server includes comprehensive error handling, request logging, and API response formatting. Development features include hot module replacement through Vite integration and automatic server restart capabilities.

## Database Design

The application uses Drizzle ORM for database schema definition and type generation. Two main entities are defined: users (for registration data) and alumni (for the alumni directory). The schema supports PostgreSQL as the target database, though the current implementation uses in-memory storage for simplicity.

User entities store registration information including name, university, college, and batch year. Alumni entities contain comprehensive profile information including designation, company, and university affiliation. The schema is designed with extensibility in mind for future enhancements.

## Authentication and Data Flow

The application implements a simple registration-based authentication system without traditional login credentials. Users register by providing their academic details, and the system creates a unique user session. Upon successful registration, users gain access to the alumni directory with full search and filtering capabilities.

The data flow follows a typical client-server pattern where the frontend makes API requests to fetch alumni data, with support for search queries and filtering by college and batch year. The backend processes these requests and returns filtered results from the alumni dataset.

# External Dependencies

## UI and Styling Framework

- **Radix UI**: Comprehensive collection of accessible, unstyled UI components
- **shadcn/ui**: Pre-built component library built on Radix UI primitives
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Lucide React**: Icon library providing consistent iconography
- **Class Variance Authority**: Utility for building variant-based component APIs

## Data Management

- **TanStack React Query**: Powerful data synchronization library for managing server state
- **React Hook Form**: Performant forms library with minimal re-renders
- **Zod**: TypeScript-first schema validation with static type inference
- **Drizzle ORM**: Lightweight TypeScript ORM with excellent type safety

## Development and Build Tools

- **Vite**: Fast build tool with hot module replacement
- **TypeScript**: Static type checking for enhanced developer experience
- **ESBuild**: Fast JavaScript/TypeScript bundler for production builds

## Database Integration

- **@neondatabase/serverless**: Serverless PostgreSQL driver for Neon database
- **Drizzle Kit**: Command-line companion for schema migrations and introspection

The application is designed to be easily deployable to cloud platforms with minimal configuration changes, supporting both development and production environments through environment-specific configurations.