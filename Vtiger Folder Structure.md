# Vtiger CRM Open Source - Folder Structure Overview

This document provides a detailed overview of the folder structure for Vtiger CRM Open Source. Each folder and file is described to help developers navigate and understand its purpose.

## **Root Directory**

- **`config.inc.php`**  
  Core configuration file containing database credentials and system settings.

- **`index.php`**  
  The main entry point for the application.

---

## **Core Folders**

### **modules/**
Contains all core and custom modules. Each module has a structured subdirectory for handling views, actions, models, event handlers, and helpers.

Example structure for a module:
```
modules/
├── Vtiger/              # Core module with shared functionality
│   ├── actions/         # Actions (e.g., AJAX or form submissions)
│   ├── models/          # Business rules and database interaction
│   ├── views/           # Views for rendering the UI in the browser
│   ├── handlers/        # Event handlers for module-specific events
│   └── helpers/         # Helper classes for module operations
├── Accounts/            # Example module: Accounts (same structure as Vtiger)
├── Leads/               # Example module: Leads
├── Contacts/            # Example module: Contacts
└── CustomModule/        # Custom modules can be added here
```

---

### **layouts/**
Contains design assets and templates for the V7 theme layout.

Structure:
```
layouts/
├── v7/                  # Layout for the V7 theme
│   ├── skins/           # CSS and styling
│   ├── resources/       # JavaScript and common resources
│   └── modules/         # Module-specific templates
│       ├── Vtiger/      # Templates and JS for the Vtiger module
│       │   ├── dashboards/  # Templates for dashboard widgets
│       │   └── resources/   # JavaScript files for views
│       ├── Accounts/    # Templates for the Accounts module
│       └── CustomModule/ # Templates for custom modules
```

---

### **user_privileges/**
Stores privilege configuration files for users.

---

### **languages/**
Contains localization files for different languages.

---

### **cron/**
Contains scripts for running scheduled tasks (cron jobs).

Structure:
```
cron/
├── vtigercron.sh            # Shell script to run Vtiger cron jobs
├── modules/com_vtiger_workflow/ # Workflow scheduler scripts
└── other_cron_scripts/      # Other cron-related tasks
```

---

### **cache/**
Stores temporary files such as compiled templates, session data, and cached images.

Structure:
```
cache/
├── images/              # Cached images
├── session/             # Session data
└── templates_c/         # Compiled templates
```

---

### **storage/**
Directory for storing uploaded files, document attachments, and other system-generated files.

---

### **logs/**
Contains log files for debugging, error tracking, and system activity monitoring.

---

### **include/**
Contains shared libraries and helper functions.

Structure:
```
include/
├── utils/               # Utility classes
├── Webservices/         # Web service classes
└── other/               # Common controllers and utility classes
```

---

### **libraries/**
Contains third-party libraries and dependencies, such as:
- **TCPDF** for generating PDFs
- **Smarty** for template rendering
- **PHPMailer** for sending emails

---

### **test/**
Contains unit and integration test files.

---

### **backup/**
Optional folder for storing database or file backups.

---

### **vtlib/**
A library for module creation, utilities, and integrations.