# InnerGrid: Building Digital Twin Platform

InnerGrid is an engineering-grade Building Digital Twin Platform engineered to capture, structure, and maintain a permanent digital record of concealed building infrastructure—including plumbing, electrical conduits, drainage, and critical building systems—across the entire property lifecycle.

---

## Table of Contents

- [Overview](#overview)
- [The Problem: Concealed Infrastructure](#the-problem-concealed-infrastructure)
- [The Solution](#the-solution)
- [Core Capabilities](#core-capabilities)
- [Target Stakeholders](#target-stakeholders)
- [System Architecture](#system-architecture)
- [Platform Workflow](#platform-workflow)
- [Security and Access Control](#security-and-access-control)
- [Project Roadmap](#project-roadmap)
- [License](#license)

---

## Overview

Modern structures conceal thousands of meters of utility pathways within structural slabs, drywall partitions, subfloors, and ceiling plenums. Once covered, the precise spatial routing and technical specifications of these systems are effectively lost to time, leading to guesswork, hazardous punctures, and destructive demolition during maintenance.

InnerGrid bridges the physical and digital domains by enabling contractors to document infrastructure during construction and renovation, translating physical installations into an interactive, high-precision digital twin. The platform serves as a permanent "digital memory" for residential and commercial structures, empowering homeowners, property managers, and field technicians with transparent visibility into what lies beneath the surface.

---

## The Problem: Concealed Infrastructure

When infrastructure issues arise—such as concealed water leaks, electrical ground faults, pipe blockages, or gas line maintenance—homeowners and maintenance teams face critical bottlenecks:

- **Missing or Inaccurate As-Built Records**: Discrepancies between initial architectural drawings and actual on-site installations frequently go untracked.
- **Destructive Exploratory Demolition**: Technicians must break through finished walls, tiles, and ceilings to locate damaged runs, incurring unnecessary repair costs and property damage.
- **Safety and Hazard Risks**: Drilling or cutting into walls blindly risks puncturing high-voltage conduits, pressurized gas pipes, or structural reinforcement.
- **Knowledge Loss During Handover**: Vital installation details known to original contractors are lost when the property transfers to new owners or facility managers.

---

## The Solution

InnerGrid replaces guesswork with verifiable spatial data. By combining mobile-first site capture, multi-modal AI documentation, and cloud-hosted digital twin representations:

- **Permanent Digital Memory**: Every conduit, joint, junction box, valve, and pipe run is recorded with precise coordinates, material metadata, and photographic proof before enclosure.
- **Non-Destructive Troubleshooting**: Technicians visualize subterranean and sub-wall routing prior to making an incision or drill point.
- **Quality Assurance Before Concealment**: Automated comparisons between architectural plans and field documentation flag deviations early in the construction phase.

---

## Core Capabilities

### 1. Infrastructure Mapping
- Comprehensive spatial logging of concealed MEP (Mechanical, Electrical, and Plumbing) networks.
- Precise positioning of junction boxes, cleanouts, shut-off valves, breakers, and service loops.
- Tagging of physical material specifications (pipe diameter, material grade, voltage ratings, manufacturer, and warranty periods).

### 2. AI-Assisted Documentation
- Intelligent extraction of spatial routes and component schedules from 2D architectural schematics and CAD/BIM exports.
- Computer vision analysis of on-site construction imagery to identify components, verify connections, and geo-locate runs relative to structural datums (columns, beams, doorframes).
- Automated transcription and organization of voice memos and field technician notes into structured component logs.

### 3. Construction-Stage Plan Verification
- Side-by-side and overlay comparison of planned schematics versus as-built photo logs.
- Discrepancy detection to identify unapproved route adjustments or omitted elements prior to dry-walling or concrete pouring.
- Digital sign-off and milestone audit trails for general contractors and inspectors.

### 4. Leakage and Fault Localization Assistance
- Targeted pathway tracing: trace supply, drainage, or circuit paths directly to isolation points (valves, breakers).
- Symptom-to-route correlation: input leak signs, moisture readings, or circuit trips to highlight high-probability concealed failure segments.
- Minimization of exploratory demolition down to targeted access points.

### 5. Centralized Digital Building Records
- Unified, cloud-hosted historical record for each property, organized by level, room, and system layer.
- Complete revision history detailing all post-construction modifications, renovations, and prior service repairs.
- Instant export of compliance dossiers, insurance documentation, and inspection certificates.

### 6. Full Lifecycle Management and Handover
- Streamlined digital handover packages from builders to real estate developers and buyers.
- Secure property transfer protocol enabling new owners to inherit the digital twin.
- Service request portal connecting homeowners with certified technicians possessing access to property-specific routing data.

---

## Target Stakeholders

| Stakeholder | Key Value Delivered |
| :--- | :--- |
| **Residential Builders and General Contractors** | Accelerate quality inspections, document compliance, and mitigate liability with immutable as-built proof. |
| **Subcontractors (Plumbers, Electricians, HVAC)** | Rapidly log installations on-site; review surrounding trades' conduits to prevent spatial clashes. |
| **Architects and Civil Engineers** | Verify design adherence and maintain a bidirectional sync between plans and field reality. |
| **Property Owners and Homeowners** | Prevent property damage during renovations, expedite emergency repairs, and maintain higher asset value. |
| **Maintenance and Facility Providers** | Eliminate diagnosis guesswork, reduce mean time to repair (MTTR), and lower customer repair expenses. |

---

## System Architecture

The InnerGrid platform consists of four primary subsystems:

```
+-------------------------------------------------------------------+
|                        Presentation Layer                         |
|   - Web Dashboard (Admin, Builders, Engineering Teams)            |
|   - Mobile Field Application (Contractor Capture & AR Viewer)     |
|   - Homeowner Portal (Service Requests & System Visualizer)       |
+-------------------------------------------------------------------+
                                  |
+-------------------------------------------------------------------+
|                          API Gateway                              |
|   - Authentication & Role-Based Access Control (RBAC)             |
|   - Tenant Isolation & Project Segmentation                       |
+-------------------------------------------------------------------+
                                  |
        +-------------------------+-------------------------+
        |                                                   |
+-------------------------------+   +-------------------------------+
|       Processing Engine       |   |       Digital Twin Engine     |
| - AI Schematic Ingestion      |   | - Spatial Coordinate Graph    |
| - Computer Vision Pipeline    |   | - Layer Isolation (MEP/Civil) |
| - Plan vs As-Built Diffing    |   | - 2D/3D Rendering & Routing   |
+-------------------------------+   +-------------------------------+
        |                                                   |
+-------------------------------------------------------------------+
|                         Data Layer                                |
|   - Spatial / Relational Database (Entities, Routes, Metadata)    |
|   - Object Storage (Raw Imagery, Video Scans, CAD/BIM Exports)    |
|   - Audit Ledger (Immutable Change History & Sign-Offs)           |
+-------------------------------------------------------------------+
```

---

## Platform Workflow

1. **Project Initiation**: Import architectural drawings, MEP schematics, and define floorplans, structural datums, and designated layers.
2. **Construction Documentation**: As trades install piping and cabling, field staff capture georeferenced photos, point clouds, or LiDAR scans prior to wall enclosure.
3. **AI Verification and Alignment**: The ingestion pipeline projects photographs onto architectural coordinate frames, mapping physical elements into the digital twin database.
4. **Discrepancy Resolution**: Any deviation from approved engineering plans is flagged for engineering review and signed off.
5. **Enclosure and Final Archival**: Once inspected, the space is sealed, and the digital twin locked as the definitive as-built baseline.
6. **Operational Maintenance**: Over the building's lifespan, authorized technicians query the twin to locate concealed infrastructure for maintenance, repairs, or future remodeling.

---

## Security and Access Control

Concealed infrastructure data includes sensitive building layouts, utility access points, and private residential details. InnerGrid implements enterprise-grade security controls:

- **Role-Based Access Control (RBAC)**: Granular permissions separate general contractors, specialized subcontractors, property owners, and temporary maintenance staff.
- **Time-Bounded Technician Access**: Homeowners can grant temporary, scoped access to specific rooms or utility layers for maintenance visits.
- **Data Encryption**: All asset data is encrypted in transit using TLS 1.3 and at rest using AES-256 encryption.
- **Immutable Audit Logging**: Every view, export, and record modification is recorded to ensure accountability.

---

## Project Roadmap

- **Phase 1: Foundation and Ingestion**
  - Project workspace creation and multi-level floorplan coordinate system.
  - Manual spatial plotting for plumbing and electrical utility runs.
  - Image and document attachment pipeline.

- **Phase 2: AI Assistance and Plan Alignment**
  - Automated detection of MEP elements from architectural drawings.
  - Photo-to-plan geo-registration using structural reference points.
  - Automated discrepancy reports (Planned vs As-Built).

- **Phase 3: Interactive Visualizer and Field App**
  - Layer-isolated 2D/3D viewer for web and tablet.
  - Augmented reality (AR) field overlay for in-situ wall inspection.
  - Route tracing and valve/breaker isolation tools.

- **Phase 4: Ecosystem and Lifecycle Tools**
  - Property transfer and digital deed handover workflows.
  - Integration with third-party BIM tools and facility management platforms.
  - Diagnostic assistant for fault and leakage root-cause analysis.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for complete terms.
