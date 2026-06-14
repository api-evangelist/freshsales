# Freshsales GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Freshsales CRM API domain model. Freshsales is the CRM application from Freshworks designed for sales teams, offering contact and account management, deal pipelines, AI-powered lead scoring, built-in phone and email, sales sequences, and CPQ.

The Freshsales REST API (https://developers.freshworks.com/crm/api/) provides CRUD access to contacts, accounts, deals, tasks, appointments, notes, and products. This GraphQL schema translates that REST surface into a typed graph of 60+ named types covering the full Freshsales data model.

## Schema Source

- Provider: Freshsales (Freshworks)
- REST API Docs: https://developers.freshworks.com/crm/api/
- GitHub: https://github.com/freshworks
- Base URL: https://<bundle-alias>.myfreshworks.com/crm/sales/api

## Type Categories

### Core CRM Objects
- Contact, ContactPhone, ContactEmail
- Company (SalesAccount)
- Lead, LeadConversion
- Deal, DealStage, DealProduct

### Pipeline and Sales Process
- Pipeline, Territory, Owner, Team

### Activities and Communication
- Activity, Task, Appointment, Meeting, Call, Note, Email, Document, File

### Users and Permissions
- User, UserRole, Role, Permission

### Marketing and Sequences
- List, Segment, Audience, Campaign, Sequence, SequenceStep, Template

### Integrations
- Webhook, Filter, Search
- EmailSync, CalendarSync, PhoneIntegration
- ChatBot, Conversation, FreshchatMessage

### CPQ (Configure, Price, Quote)
- Product, ProductVariant, Tax, Discount, Quote, Order, Invoice, Payment

### Intelligence (Freddy AI)
- LeadScore, ContactScore, FreddyAI, SmartMatch, Intent, ContextData

### Platform
- APIKey, OAuthToken, SalesAccountContact, Report, FunnelReport

## Usage Notes

Authentication uses a token-based scheme via the `Authorization: Token token=<api_key>` header, scoped to a bundle-alias-specific subdomain. All API calls are tenant-scoped to the Freshsales account subdomain.
