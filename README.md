# Streambit.Catalog.Infrastructure

This project represents the **Infrastructure layer** of the Streambit Catalog solution, following Clean Architecture principles.

## Overview

The Infrastructure layer provides concrete implementations of application contracts, including:

- **Persistence**  
  Entity Framework Core `DbContext` and repository implementations.  

- **Data Access Logic**  
  Query optimizations and potential support for alternative ORMs (e.g., Dapper).  

- **Integration Points**  
  External infrastructure concerns such as databases, messaging, and third-party services.  

## Dependencies

- **Domain**: for aggregates, entities, and value objects.  
- **Application**: for repository interfaces and application contracts.  

## Architecture Note

The Infrastructure layer **depends on Domain and Application**, but neither `Domain` nor `Application` depend on Infrastructure.  
This ensures proper separation of concerns and provides flexibility to switch or extend technologies without affecting business logic.  
