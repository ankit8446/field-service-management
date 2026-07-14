# Business Discovery Document
### SunVolt Energy Services Pvt Ltd

---

## 1. Client Overview

| Detail | Information |
|---|---|
| Company Name | SunVolt Energy Services Pvt Ltd |
| Industry | Residential & Commercial Solar Services |
| Company Type | Solar EPC (Engineering, Procurement, Construction) + Service Provider |
| Target Market | Residential homeowners, Commercial establishments, Industrial clients |

---

## 2. Services Offered

| Service Type | Description | Frequency |
|---|---|---|
| Installation | New solar panel system installation | Project-based |
| AMC (Annual Maintenance Contract) | Preventive maintenance, regular inspections, cleaning | Yearly contract |
| Emergency Repair | Urgent breakdown repair, system failure | On-demand |
| Warranty Support | Manufacturer warranty claims, replacement | As needed |
| Site Inspection | Pre-installation survey, feasibility assessment | Project-based |

---

## 3. Current Process (AS-IS)

```
CUSTOMER CALLS/WHATSAPP ──► OPERATIONS TEAM ──► EXCEL SHEET
                                    │
                                    ▼
                             TECHNICIAN (Phone Call)
                                    │
                                    ▼
                         PAPER JOB SHEET (Manual Entry)
                                    │
                                    ▼
                        BACK TO OFFICE (Excel Update)
```

**Tools Currently Used:** Phone Calls, WhatsApp, Excel Spreadsheets, Paper Job Sheets

---

## 4. Current Pain Points

### 4.1 Technician Scheduling
- No visibility into technician availability
- Manual assignment via phone calls
- No skill-based matching
- No route optimization
- Duplicate/overlapping assignments

### 4.2 No Centralized Tracking
- Information scattered across Excel, WhatsApp, Paper
- No single source of truth
- Status updates not real-time
- Cannot track job progress
- Historical data not searchable

### 4.3 Delayed Updates
- Customer doesn't know when technician will arrive
- Management doesn't know job status
- Updates only after job completion
- No live tracking
- No automated notifications

### 4.4 Paper-Based Reports
- Job sheets filled manually
- Prone to errors and illegible handwriting
- Photos attached separately
- Lost/damaged reports
- No digital signatures
- Difficult to archive and retrieve

### 4.5 Poor Customer Communication
- No automated appointment reminders
- Customers wait without updates
- No real-time technician arrival alerts
- No digital job completion confirmation
- No feedback mechanism
- No service history visibility

### 4.6 Difficult Reporting
- Manual data compilation for reports
- Time-consuming monthly/quarterly reports
- No real-time dashboards
- Cannot generate performance metrics
- No trend analysis
- Decision-making based on incomplete data

---

## 5. Business Goals

| Goal | Description |
|---|---|
| Digitize Field Operations | Replace paper with digital job sheets, real-time updates, centralized data |
| Improve Technician Productivity | Smart scheduling, route optimization, reduce travel time, increase jobs per day |
| Improve Customer Visibility | Real-time tracking, automated notifications, service history access |
| Reduce Manual Work | Automated workflows, digital forms, auto-generated reports, 80% data entry reduction |

---

## 6. Expected Product — Architecture Overview

```
┌─────────────────────┐        ┌─────────────────────────────────┐
│      MOBILE APP       │        │           WEB PORTAL             │
│      (Technician)     │        │        (Operations Team)         │
│                       │        │                                   │
│ • View assigned jobs │        │ • Dashboard & Analytics           │
│ • Update status       │        │ • Customer Management            │
│ • Capture photos      │        │ • Technician Management          │
│ • Digital signature   │        │ • Work Order Creation            │
│ • Navigation           │        │ • Scheduling & Assignment        │
│ • Timesheet            │        │ • Reporting & Export             │
│                       │        │ • Service History                 │
└──────────┬────────────┘        └──────────────┬────────────────────┘
           │                                     │
           └─────────────────┬───────────────────┘
                              │
                              ▼
                ┌───────────────────────────────┐
                │          BACKEND APIs           │
                │  • REST APIs                    │
                │  • Authentication                │
                │  • Database                       │
                │  • Notifications                  │
                │  • File Storage                   │
                └───────────────────────────────┘
```

**Components:**
- Mobile App — For Technicians
- Web Portal — For Operations Team
- Backend APIs — For all functionality

> **Note:** Nothing technical beyond this scope.

---

## 7. Success Criteria

### 7.1 Reduce Manual Work
| Current | Target |
|---|---|
| 100% manual data entry | 20% manual (80% reduction) |
| Paper job sheets | Digital forms on mobile |
| Manual Excel reporting | Auto-generated reports |
| Phone-based updates | In-app status updates |

### 7.2 Track Technicians
| Current | Target |
|---|---|
| Unknown location | Real-time GPS tracking |
| Phone calls to check status | Live status in dashboard |
| Manual timesheets | Auto-capture check-in/out |
| No productivity data | Performance analytics |

### 7.3 Improve Scheduling
| Current | Target |
|---|---|
| Manual phone-based assignment | Auto-assignment based on skills |
| Overlapping jobs | Smart scheduling |
| No availability view | Real-time calendar view |
| No route planning | Optimized route suggestions |

### 7.4 Maintain Service History
| Current | Target |
|---|---|
| Scattered data | Centralized customer history |
| No searchability | Full-text search |
| No customer view | Customer portal access |
| Missing records | Complete audit trail |

### 7.5 Capture Job Completion Evidence
| Current | Target |
|---|---|
| No photos | Photos captured in app |
| Verbal confirmations | Digital signatures |
| No before/after | Before/after image capture |
| No proof of work | Complete digital job report |

### 7.6 Generate Reports
| Current | Target |
|---|---|
| Manual compilation | Auto-generated reports |
| Monthly only | Real-time dashboards |
| Limited metrics | Comprehensive analytics |
| Excel-based | Web-based with export |

---

## 8. Proposed Modules

**Module 1: Customer Management**
- Add/Edit/View Customers, Search & Filter, Service History, AMC Details, Equipment Details, Communication Log

**Module 2: Technician Management**
- Add/Edit/View Technicians, Skills Management, Availability Calendar, Performance Analytics, Attendance Tracking, Assignment History

**Module 3: Work Order Management**
- Create Work Order (AMC, Emergency, Installation), Assign Technician (Auto/Manual), Status Tracking (Pending → Assigned → In Progress → Completed → Closed), Priority Management (High/Medium/Low), Scheduling, History & Audit Log

**Module 4: Mobile App (Technician)**
- Today's Jobs List, Job Details View, Start/Complete Job, Capture Photos (Before/After), Digital Signature, Navigation/Route, Offline Support, Attendance (Check-in/Check-out)

**Module 5: Reporting & Analytics**
- Operations Dashboard, Technician Performance Reports, Customer Service History Reports, AMC Renewal Reports, Revenue Reports, Export (PDF/Excel), Custom Report Builder

**Module 6: Communication**
- Automated SMS, Email Notifications, In-App Notifications, Customer Alerts (Technician arrival, job completion), Follow-up Automation, WhatsApp Integration (Optional)

---

## 9. Workflow Diagram (TO-BE)

| Customer | Operations Team | Technician |
|---|---|---|
| Requests Service (Call/App) | Creates Work Order, Assigns Technician, Sends Notification | Receives Notification, Views Job in App |
| Gets SMS with ETA | Sees Status Updated (Real-time) | Accepts Job, Starts Journey, GPS Tracking Active |
| Technician Arrives | — | Arrives at Site, Marks Arrival |
| Gets SMS "Job Done" | Receives Report, Generates Invoice | Completes Work, Captures Photos, Gets Digital Signature |
| Gives Feedback | Updates History | Completes Job, Marks Done |
| Gets Follow-up | Auto Follow-up | Ready for Next Job |

---

## 10. KPI Dashboard Metrics

| KPI Category | Metrics |
|---|---|
| Operations | Total jobs, Jobs by status, Jobs by type (AMC/Emergency/Installation) |
| Technician | Utilization rate, Jobs per tech, Average job duration, On-time arrival % |
| Customer | Wait time, Satisfaction rating (CSAT), Repeat business rate, Response time |
| Financial | Revenue per job, AMC renewal rate, Cost per job |

---

## 11. Estimated Project Metrics

| Metric | Target |
|---|---|
| Technician Productivity | +30% (more jobs per day) |
| Scheduling Time | Reduced by 80% |
| Paper Usage | Reduced by 95% |
| Customer Response Time | Reduced by 70% |
| Report Generation Time | From days to minutes |
| Customer Satisfaction | Target: 4.5/5 |
| AMC Renewal Rate | Increase by 20% |
| Data Entry Errors | Reduced by 90% |

---

## 12. Technology Recommendations (Paid / Standard Options)

**Backend**
| Component | Recommendation |
|---|---|
| Framework | Node.js + Express.js OR Python + Django |
| Database | PostgreSQL (Recommended) OR MongoDB |
| Authentication | JWT |
| File Storage | AWS S3 / Cloudinary |
| SMS | Twilio |
| Email | SendGrid |
| Hosting | AWS / DigitalOcean / Render |
| API | RESTful APIs |

**Web Portal**
| Component | Recommendation |
|---|---|
| Framework | React.js OR Next.js |
| UI Library | Ant Design OR Material-UI |
| Charts | Chart.js / Recharts |
| Maps | Google Maps API / Mapbox |
| Hosting | Vercel / Netlify |

**Mobile App**
| Component | Recommendation |
|---|---|
| Framework | React Native OR Flutter |
| Features | GPS, Camera, Offline Storage |
| Map | Google Maps SDK |
| Distribution | Google Play Store + Apple App Store |

---

## 12A. Zero-Budget Technology Stack (Free-Tier Alternatives)

Since there's no budget to start with, here's a stack that lets you build and run the entire MVP on free tiers. Good enough for development, demos, and early pilot usage with a handful of technicians. You'll likely outgrow some limits once usage scales — that's the point at which you start paying.

### Database
| Purpose | Free Option | Free Limit |
|---|---|---|
| Primary DB (NoSQL) | **MongoDB Atlas (M0 Free Cluster)** | 512 MB storage, shared cluster, forever free |
| Primary DB (SQL alternative) | **Supabase (Postgres)** | 500 MB DB, 2 free projects, built-in auth + storage |
| Alternative | **Neon.tech (Postgres)** | 512 MB, serverless, generous free tier |

> Recommendation: MongoDB Atlas free tier is a good fit here since work orders, job sheets, and technician logs are naturally document-shaped (flexible fields, photos, nested status history).

### Backend Hosting
| Purpose | Free Option | Notes |
|---|---|---|
| API Hosting | **Render (Free Web Service)** | Free but sleeps after inactivity (cold start ~30s) |
| API Hosting (alt) | **Railway.app (Free tier / trial credits)** | Good DX, limited free hours/month |
| Serverless functions | **Vercel Serverless / Netlify Functions** | Good for lightweight APIs |

### Authentication
| Purpose | Free Option | Notes |
|---|---|---|
| Auth | **Firebase Authentication** | Free up to 50K monthly active users |
| Auth (alt) | **Supabase Auth** | Free, integrated if you use Supabase DB |

### Maps & Location (instead of Google Maps API, which needs a billing account)
| Purpose | Free Option | Notes |
|---|---|---|
| Maps + Tiles | **OpenStreetMap + Leaflet.js** | 100% free, no API key, no billing card needed |
| Maps SDK (mobile) | **react-native-maps with OSM tiles** or **Mapbox Free Tier** | Mapbox gives 50,000 free map loads/month |
| Geocoding | **OpenStreetMap Nominatim (free)** or **Mapbox Geocoding (free tier)** | Nominatim has fair-use rate limits |
| Route Optimization | **OSRM (Open Source Routing Machine)** — free, self-hosted or public demo server | Good enough for basic route suggestions |

> Google Maps also gives $200/month free credit, which is usable, but it requires adding a credit card — OpenStreetMap/Leaflet avoids that entirely for a true zero-cost start.

### File Storage (for job photos, signatures)
| Purpose | Free Option | Free Limit |
|---|---|---|
| Image/File Storage | **Cloudinary Free Tier** | 25 GB storage + 25 GB bandwidth/month, image transformations included |
| Alternative | **Firebase Storage** | 5 GB free storage |
| Alternative | **Supabase Storage** | 1 GB free (bundled with Supabase project) |

### SMS Notifications
| Purpose | Free Option | Notes |
|---|---|---|
| SMS (India-focused) | **Fast2SMS** | Free trial credits, pay-as-you-go after, India-friendly |
| SMS (India-focused alt) | **MSG91** | Free trial credits, good India delivery rates |
| SMS (global) | **Twilio Free Trial** | ~$15 trial credit, needs verified numbers during trial |
| WhatsApp alerts (free-ish) | **WhatsApp Cloud API (Meta)** | Free tier: 1,000 conversations/month |

### Email Notifications
| Purpose | Free Option | Free Limit |
|---|---|---|
| Transactional Email | **Brevo (formerly Sendinblue)** | 300 emails/day free, forever |
| Alternative | **SendGrid Free Tier** | 100 emails/day free |
| Alternative | **Resend.com** | 3,000 emails/month free |

### Push Notifications (in-app)
| Purpose | Free Option |
|---|---|
| Push Notifications | **Firebase Cloud Messaging (FCM)** — completely free, unlimited |

### Frontend / Web Portal Hosting
| Purpose | Free Option |
|---|---|
| Web Portal Hosting | **Vercel** or **Netlify** — both have generous free tiers for React/Next.js apps |

### Mobile App
| Purpose | Free Option |
|---|---|
| Framework | **React Native (Expo)** — completely free/open-source, no cost to build or test |
| Distribution (testing) | **Expo Go app** or **Expo EAS free tier builds** — test without paying developer fees during dev phase |
| Play Store listing | One-time $25 (only real unavoidable cost, when ready to publish) |
| App Store listing | $99/year (only needed when publishing to iOS App Store — can be deferred, start Android-only) |

### Suggested Zero-Budget MVP Stack Summary
| Layer | Free Choice |
|---|---|
| Database | MongoDB Atlas (Free M0) |
| Backend | Node.js + Express, hosted on Render (Free) |
| Auth | Firebase Authentication |
| File Storage | Cloudinary (Free) |
| Maps | OpenStreetMap + Leaflet / Mapbox Free Tier |
| SMS | Fast2SMS / MSG91 (India) |
| Email | Brevo (300/day free) |
| Push Notifications | Firebase Cloud Messaging |
| Web Portal | React.js, hosted on Vercel (Free) |
| Mobile App | React Native (Expo), tested via Expo Go |

**Realistic caveats to plan for:**
- Free-tier backend hosting (Render) sleeps when idle — fine for a demo/pilot, not for production with real customers expecting instant responses.
- MongoDB Atlas free tier (512 MB) is enough for a few hundred to low-thousands of work orders/customers, not years of scaled data.
- SMS free credits run out fast — budget a small recurring cost (a few hundred rupees/month) once you're live with real customers, since SMS is rarely fully free at scale.
- iOS publishing has an unavoidable $99/year fee — you can launch Android-first and add iOS later once there's revenue.

---

## 12B. Reference Applications — Study Features, Not UI

Before/while building, it's far more valuable to study how established field-service platforms **structure their workflows** than to try to copy their screens. Watch product demo videos (YouTube, official demo pages) rather than just screenshots — you'll absorb the *why* behind each feature, not just the look.

| App | Best For Studying | Notes |
|---|---|---|
| **Salesforce Field Service** | Complete end-to-end workflow, industry standard | Enterprise-grade — look at how work orders flow from creation to closure |
| **ServiceTitan** | Closest match to SunVolt's business (HVAC, plumbing, solar) | Very relevant — study their scheduling, dispatch, and AMC/maintenance contract handling |
| **Jobber** | Scheduling simplicity | Great reference for a clean, simple scheduling/calendar UX without enterprise bloat |
| **Housecall Pro** | Customer-facing workflow | Good for studying booking, notifications, and customer communication flow |
| **Microsoft Dynamics 365 Field Service** | Enterprise FSM patterns | Useful for understanding large-scale resource scheduling and reporting structures |
| **Zoho FSM** | Easiest to understand overall | Good starting point — simpler feature set, easier to map to SunVolt's Phase 1-2 scope |

**How to use this list effectively:**
1. Watch official product demo videos for each (not just marketing pages).
2. For each, note: how a job/work order moves through statuses, how technicians are assigned, what the customer sees at each step, and what shows up on the dashboard.
3. Map those patterns back to SunVolt's own **Modules 1–6** (Section 8) — most of what these platforms do already exists in outline form there.
4. Don't chase feature parity with enterprise tools like Salesforce/Microsoft — study them for concepts, but build to the scope in the Phase-Wise Delivery Plan (Section 14).

---

## 13. Go-to-Market & Local Customer Acquisition Strategy

Getting the software right solves the *operations* problem. This section covers how SunVolt actually gets customers in their service area — mostly low-cost/no-cost channels suited to a local solar EPC business.

### 13.1 Free / Low-Cost Digital Channels
| Channel | What to Do | Why It Works |
|---|---|---|
| **Google Business Profile** | Claim & fully optimize listing (photos, service area, reviews, posts) | Free, and the #1 way people search "solar installer near me" |
| **Local SEO** | Simple landing page targeting "solar panel installation in [city/area]" | Captures high-intent search traffic without ad spend |
| **WhatsApp Business** | Catalog of services, auto-replies, broadcast lists for past customers | Customers in India already live on WhatsApp — near-zero cost |
| **Referral Program** | Small discount/cashback for existing customers who refer new ones | Solar is trust-heavy — referrals convert far better than ads |
| **Facebook/Instagram local groups** | Post case studies, before/after installs, subsidy info in local housing/community groups | Free reach into hyper-local audiences |
| **YouTube/Instagram Reels** | Short videos: installation process, savings explained, customer testimonials | Builds trust before first contact, cheap to produce |

### 13.2 Local Partnerships & Tie-Ups
| Partner Type | Approach |
|---|---|
| **Electricians & Contractors** | Commission-based referral tie-ups — they already visit homes needing electrical work |
| **Real Estate Agents / Builders** | Partner for new construction/villa projects — bundle solar at handover |
| **RWAs (Resident Welfare Associations)** | Present to housing societies — bulk/society-wide discounts drive group sign-ups |
| **Electrical/Hardware Shops** | Leave brochures/referral incentives at shops solar customers already visit |

### 13.3 Government Scheme Leads (India-specific)
- **PM Surya Ghar Muft Bijli Yojana** (rooftop solar subsidy scheme) — many customers specifically search for **empanelled/subsidy-eligible vendors**. Getting SunVolt registered as an empanelled vendor on the relevant state DISCOM/national portal is one of the highest-leverage, lowest-cost lead sources available.
- Attend local **DISCOM or MNRE-organized awareness camps** — direct access to subsidy-seeking homeowners.

### 13.4 Targeted Local Outreach
- **High electricity bill targeting**: Partner with local electricians/meter readers informally, or target housing societies known for large homes/high consumption.
- **Door-to-door campaigns** in specific residential areas, backed by a simple flyer with QR code to WhatsApp/landing page.
- **Commercial cold outreach**: Small factories, schools, hospitals, shops — these have high daytime power usage, making solar ROI pitch strong.

### 13.5 Retention → Acquisition Loop
Since SunVolt already plans AMC (Annual Maintenance Contracts), every AMC visit is a touchpoint:
- Use the mobile app's **customer feedback + photo evidence** (Module 4/5) as **social proof material** for marketing.
- Auto-trigger a **referral request SMS/WhatsApp** after every successfully closed job (tie this into Module 6: Communication).
- Track **referral source** as a field in Customer Management (Module 1) so you know which channel is actually working — data-driven marketing spend later.

### 13.6 Reference: Where to Study Proven Field-Service Playbooks
See Section 12B above — companies like ServiceTitan and Housecall Pro also publish content on how their customers (HVAC, plumbing, solar contractors) generate local leads. Their blogs/case studies are a free source of go-to-market ideas, not just product features.

---

## 14. Phase-Wise Delivery Plan

| Phase | Duration | Deliverables |
|---|---|---|
| Phase 1: Foundation | Weeks 1-2 | Database Design, Authentication, Basic Backend APIs, Admin Dashboard (Basic), Technician & Customer CRUD |
| Phase 2: Core Features | Weeks 3-4 | Work Order Creation & Assignment (Manual), Technician Mobile App (Job List), Status Updates, Basic SMS Notifications |
| Phase 3: Advanced Features | Weeks 5-6 | Auto-Assignment (Skill-based), GPS Tracking, Photo Capture, Digital Signature, Customer Notifications, Job Completion Reports |
| Phase 4: Analytics & Reporting | Weeks 7-8 | Real-time Dashboard, Performance Reports, AMC Reports, Revenue Reports, Export, Service History |
| Phase 5: Enhancements | Weeks 9-10 | Advanced Search, Offline Support (Mobile), Customer Portal (Basic), Follow-up Automation, Feedback Management, UAT & Bug Fixes |

---

## 15. Next Steps / Clarification Questions

Questions to Ask Client:
1. Do you have existing customer data in Excel? (For migration planning)
2. How many technicians currently work with you? (For scalability)
3. Which SMS service do you currently use? (For integration)
4. Do you need multi-city support? (For scope definition)
5. What's your budget for hosting/third-party services?
6. Do you want a customer app or customer web portal?
7. What are your peak hours for service calls?
8. Do you have existing AMC contracts to migrate?

---

## 16. Document Version History

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-07-08 | [Developer Name] | Initial business discovery document created |
| 1.1 | 2026-07-08 | [Developer Name] | Added Zero-Budget Technology Stack section (12A) |
| 1.2 | 2026-07-08 | [Developer Name] | Added Go-to-Market/Customer Acquisition Strategy (13) and Reference Applications section (12B) |

---

## 17. Approvals

| Role | Name | Signature | Date |
|---|---|---|---|
| Client | [Client Name] | | |
| Project Manager | [PM Name] | | |
| Lead Developer | [Dev Name] | | |

---

**Document Status:** ✅ FINAL - Ready for Development
