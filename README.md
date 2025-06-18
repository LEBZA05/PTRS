# Proficiency Test System (PTRS)

A comprehensive laboratory proficiency test management system built with React, TypeScript, and Supabase.

## Features

- **Multi-role Authentication**: Support for IT Officers, Lab Technicians, Hospital Staff, and Lab Managers
- **Test Request Management**: Hospital staff can request lab tests with priority levels
- **Result Validation Workflow**: Lab technicians upload results, lab managers validate them
- **Real-time Notifications**: Instant notifications for all stakeholders
- **File Upload**: Secure lab report storage and management
- **Dashboard Analytics**: Role-specific dashboards with comprehensive data views
- **Search Functionality**: Advanced search capabilities for test results

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Backend**: Supabase (PostgreSQL, Authentication, Storage, Real-time)
- **Icons**: Lucide React
- **Charts**: Recharts
- **Routing**: React Router DOM
- **State Management**: React Query (TanStack Query)
- **Notifications**: React Hot Toast

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Supabase account

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd proficiency-test-system
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env` file in the root directory:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Run the development server:
```bash
npm run dev
```

5. Open [http://localhost:5173](http://localhost:5173) in your browser.

## Database Setup

The project includes comprehensive database migrations in the `supabase/migrations` folder. These migrations set up:

- User role tables (IT Officers, Lab Technicians, Hospital Staff, Lab Managers)
- Test request and result management
- Notification system
- File storage policies
- Row Level Security (RLS) policies

## User Roles

### IT Officer
- Manage all user accounts and approvals
- View system analytics and reports
- Configure system settings
- Manage system alerts

### Lab Technician
- View and accept test requests
- Upload test results and reports
- Send validated results to hospital staff
- Track result validation status

### Lab Manager
- Validate test results from lab technicians
- Review and approve/reject lab reports
- Monitor lab performance metrics
- Manage quality control processes

### Hospital Staff
- Submit test requests with priority levels
- View validated test results
- Download lab reports
- Track request status

## Key Features

### Validation Workflow
1. Hospital staff submits test request
2. Lab technician accepts and processes request
3. Lab technician uploads results (pending validation)
4. Lab manager validates results
5. Validated results become available to hospital staff

### Real-time Notifications
- Instant notifications for new requests, results, and validations
- Email notification options
- Custom message support

### Security
- Row Level Security (RLS) on all tables
- Role-based access control
- Secure file upload and storage
- Email-based authentication

## Deployment

### Netlify (Recommended)
The project is configured for easy Netlify deployment:

```bash
npm run build
```

Deploy the `dist` folder to Netlify.

### Manual Deployment
1. Build the project: `npm run build`
2. Deploy the `dist` folder to your hosting provider
3. Configure environment variables on your hosting platform

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -am 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, please contact the development team or create an issue in the repository.