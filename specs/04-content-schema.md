# 04. Content Schema: Structured Content for The CKB Firm Website

This document defines the content types, fields, relationships, and SEO requirements for The CKB Firm's website, designed for a headless CMS.

## I. Content Types

### 1. Page
*   **Purpose:** Flexible content structure for static pages (e.g., About Us, Contact Us, Privacy Policy, Terms of Service).
*   **Fields:**
    *   `title` (Text): Page Title (e.g., "About Us") - **Required**
    *   `slug` (Slug): URL slug (e.g., `about-us`) - **Required, Unique, Auto-generated with manual override**
    *   `heroHeadline` (Text): Main headline for the hero section - **Optional**
    *   `heroSubheadline` (Rich Text): Supporting text for the hero section - **Optional**
    *   `heroImage` (Asset): Background image for the hero section - **Optional**
    *   `sections` (Flexible Content Block): A repeatable block allowing for various content components (see below). - **Required (at least one)**
    *   `seo` (Group/Embed): See SEO Requirements section.

### 2. Service
*   **Purpose:** Detailed information about each legal service offered.
*   **Fields:**
    *   `name` (Text): Service Name (e.g., "Commercial Litigation") - **Required**
    *   `slug` (Slug): URL slug (e.g., `commercial-litigation`) - **Required, Unique, Auto-generated with manual override**
    *   `introHeadline` (Text): Short, punchy headline for the service overview - **Required**
    *   `introSubheadline` (Rich Text): Brief introduction to the service - **Required**
    *   `heroImage` (Asset): Featured image for the service page hero - **Optional**
    *   `fullDescription` (Rich Text): Detailed description of the service, including its scope and benefits - **Required**
    *   `keyServicesList` (List of Text): Bullet points or short descriptions of specific sub-services (e.g., "Breach of Contract", "Pre-suit") - **Required**
    *   `processSteps` (List of Group): Repeatable group for outlining process. Each group has:
        *   `stepHeadline` (Text): (e.g., "Initial Assessment & Strategy") - **Required**
        *   `stepDescription` (Rich Text): - **Required**
    *   `serviceAdvantages` (List of Group): Repeatable group for highlighting unique advantages. Each group has:
        *   `advantageHeadline` (Text): (e.g., "Unrivaled Expertise") - **Required**
        *   `advantageDescription` (Rich Text): - **Required**
    *   `relatedAttorneys` (Reference): Multi-reference to `Attorney` content type. - **Required**
    *   `seo` (Group/Embed): See SEO Requirements section.

### 3. Attorney
*   **Purpose:** Individual profiles for each legal professional at the firm.
*   **Fields:**
    *   `fullName` (Text): Attorney's full name (e.g., "Michael S. Baim") - **Required**
    *   `slug` (Slug): URL slug (e.g., `michael-baim`) - **Required, Unique, Auto-generated with manual override**
    *   `title` (Text): Professional Title (e.g., "Managing Partner") - **Required**
    *   `photo` (Asset): Professional headshot - **Required**
    *   `email` (Text): Direct email address - **Required**
    *   `phone` (Text): Direct phone number - **Optional**
    *   `shortBioSnippet` (Text): Brief summary for cards/listings - **Required**
    *   `fullBiography` (Rich Text): Detailed professional biography - **Required**
    *   `barAdmissions` (List of Text): (e.g., "Illinois, 1990") - **Required**
    *   `education` (List of Rich Text): (e.g., "Chicago Kent College of Law, Chicago, Illinois (J.D.)") - **Required**
    *   `pastEmployment` (List of Text): (e.g., "Baim & Lepak, LLC., Managing Partner") - **Optional**
    *   `practiceAreas` (Reference): Multi-reference to `Service` content type. - **Required**
    *   `linkedinProfile` (URL): Link to LinkedIn profile - **Optional**
    *   `seo` (Group/Embed): See SEO Requirements section.

### 4. Article (for "Insights" section)
*   **Purpose:** Thought leadership, legal updates, firm news.
*   **Fields:**
    *   `title` (Text): Article Title - **Required**
    *   `slug` (Slug): URL slug (e.g., `navigating-breach-of-contract-chicago`) - **Required, Unique, Auto-generated with manual override**
    *   `author` (Reference): Single reference to `Attorney` content type. - **Required**
    *   `publishDate` (Date): Date of publication - **Required**
    *   `featuredImage` (Asset): Image for article card and hero - **Required**
    *   `excerpt` (Textarea): Short summary for listings - **Required**
    *   `bodyContent` (Rich Text): Full article content - **Required**
    *   `category` (Dropdown/Tags): (e.g., "Commercial Litigation," "Creditors' Rights," "Real Estate Law," "Firm News") - **Required**
    *   `tags` (Tags): Keywords for filtering/search - **Optional**
    *   `seo` (Group/Embed): See SEO Requirements section.

### 5. Testimonial
*   **Purpose:** Client endorsements.
*   **Fields:**
    *   `clientName` (Text): Client's name or "Anonymous" - **Required**
    *   `clientTitleCompany` (Text): Client's title and/or company (e.g., "CEO, [Company Name]") - **Optional**
    *   `quote` (Textarea): The full testimonial quote - **Required**
    *   `relatedService` (Reference): Single reference to `Service` content type (if applicable) - **Optional**

### 6. Affiliation
*   **Purpose:** Professional memberships and certifications.
*   **Fields:**
    *   `name` (Text): Organization Name (e.g., "Commercial Law League of America") - **Required**
    *   `logo` (Asset): Organization's logo - **Required**
    *   `websiteUrl` (URL): Link to the organization's website - **Optional**

### 7. Location
*   **Purpose:** Firm's physical address and contact details.
*   **Fields:**
    *   `name` (Text): Location Nickname (e.g., "Main Office") - **Required**
    *   `streetAddress` (Text): (e.g., "125 S. Clark Street Suite 1700") - **Required**
    *   `city` (Text): (e.g., "Chicago") - **Required**
    *   `state` (Text): (e.g., "IL") - **Required**
    *   `zipCode` (Text): (e.g., "60603") - **Required**
    *   `country` (Text): (e.g., "USA") - **Required**
    *   `phoneNumber` (Text): (e.g., "+1 (312) 704-8510") - **Required**
    *   `generalEmail` (Text): (e.g., "info@ckbfirm.com") - **Required**
    *   `googleMapsLink` (URL): Direct link to Google Maps for directions - **Required**
    *   `officeHours` (Rich Text): (e.g., "Monday - Friday: 9:00 AM - 5:00 PM CST") - **Optional**

### 8. Call to Action (Reusable Component)
*   **Purpose:** Define reusable CTA blocks.
*   **Fields:**
    *   `buttonText` (Text): (e.g., "Request a Consultation") - **Required**
    *   `buttonLink` (URL): Internal or external URL - **Required**
    *   `style` (Dropdown): (e.g., "Primary", "Secondary", "Ghost") - **Required**
    *   `icon` (Asset): Optional icon to display next to button text - **Optional**

## II. Flexible Content Blocks (for `Page` content type)

These blocks allow page editors to construct custom layouts for generic pages.

1.  **Rich Text Block:**
    *   `content` (Rich Text): Standard text, headings, lists, links.
2.  **Image Block:**
    *   `image` (Asset): Image file.
    *   `caption` (Text): Optional image caption.
3.  **Two Column Text Block:**
    *   `column1Content` (Rich Text)
    *   `column2Content` (Rich Text)
4.  **CTA Block:**
    *   `headline` (Text): Optional headline above CTA.
    *   `copy` (Rich Text): Optional descriptive text.
    *   `cta` (Reference): Reference to `Call to Action` content type.
5.  **Testimonial Slider Block:**
    *   `testimonials` (Reference): Multi-reference to `Testimonial` content type.
6.  **Attorney Grid Block:**
    *   `headline` (Text)
    *   `subheadline` (Rich Text)
    *   `attorneys` (Reference): Multi-reference to `Attorney` content type.
7.  **Service Grid Block:**
    *   `headline` (Text)
    *   `subheadline` (Rich Text)
    *   `services` (Reference): Multi-reference to `Service` content type.
8.  **Affiliations Grid Block:**
    *   `headline` (Text)
    *   `subheadline` (Rich Text)
    *   `affiliations` (Reference): Multi-reference to `Affiliation` content type.

## III. Relationships

*   **Service -> Attorney:** A Service can be associated with multiple Attorneys who practice in that area. An Attorney can be associated with multiple Services. (Many-to-Many)
*   **Article -> Attorney:** An Article has one Author (Attorney). (Many-to-One)
*   **Testimonial -> Service:** A Testimonial can be optionally linked to a specific Service. (Many-to-One)
*   **Page -> Flexible Content Blocks -> CTA:** Pages can embed reusable CTA components.
*   **Page -> Flexible Content Blocks -> Attorney/Service/Affiliation/Testimonial:** Pages can display grids/sliders of these content types.

## IV. SEO Requirements (Embedded Group for all relevant content types)

All `Page`, `Service`, `Attorney`, and `Article` content types will have an embedded `seo` group with the following fields:

*   `metaTitle` (Text): Page title for search engines (max 60 characters) - **Required**
*   `metaDescription` (Textarea): Page description for search engines (max 160 characters) - **Required**
*   `canonicalUrl` (URL): Canonical URL, auto-populated but editable for advanced use cases - **Optional**
*   `ogTitle` (Text): Open Graph Title (for social sharing, defaults to `metaTitle`) - **Optional**
*   `ogDescription` (Textarea): Open Graph Description (for social sharing, defaults to `metaDescription`) - **Optional**
*   `ogImage` (Asset): Open Graph Image (for social sharing, defaults to `featuredImage` or global default) - **Optional**
*   `noIndex` (Boolean): Checkbox to prevent search engine indexing - **Optional (defaults to false)**
*   `noFollow` (Boolean): Checkbox to prevent search engine following links - **Optional (defaults to false)**

## V. CMS Structure & User Experience

*   **Content Tree:** A clear, hierarchical content tree reflecting the site's navigation structure.
*   **Search & Filtering:** Easy search and filtering capabilities within the CMS to quickly locate content.
*   **Preview Functionality:** Real-time or draft preview functionality to see how content will appear on the live site before publishing.
*   **Versioning:** Ability to revert to previous versions of content.
*   **Localization (Future-Proofing):** The schema should be designed to support multiple languages if the firm expands internationally, though not an immediate requirement.
*   **Asset Management:** Drag-and-drop uploads, folders for organization, automatic image optimization and resizing upon upload.

This content schema provides a robust and flexible foundation for The CKB Firm's new website, enabling efficient content management, strong SEO, and a dynamic user experience.