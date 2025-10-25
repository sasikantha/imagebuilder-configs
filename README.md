# Image Builder Configurations

This repository contains AWS Image Builder components and recipes managed through GitOps workflow.

## Structure

```
components/          # Image Builder components
├── web-server.yaml
└── security-hardening.yaml

recipes/            # Image Builder recipes  
└── web-server-recipe.yaml

.github/workflows/  # GitHub Actions
└── imagebuilder.yml
```

## Workflow

1. **Edit** components or recipes
2. **Commit** changes to main branch
3. **GitHub Actions** automatically updates Image Builder
4. **Pipeline** triggers and builds new AMI
5. **Lambda** updates Auto Scaling Group

## Components

### web-server.yaml
- Installs Apache HTTP server
- Creates basic web content
- Enables service

### security-hardening.yaml
- Updates security packages
- Configures firewall
- Hardens SSH configuration

## Usage

Changes to this repository automatically trigger Image Builder pipeline execution through GitHub Actions integration.
