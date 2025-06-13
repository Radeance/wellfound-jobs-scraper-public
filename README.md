# 💎 Wellfound Premium Jobs Scraper

![Wellfound Job Listings](https://i.imgur.com/q5KaXPd.png)
| Try our other scrapers ► | [Glassdoor Premium Jobs Scraper](https://apify.com/radeance/glassdoor-jobs-scraper) | [Similarweb Scraper](https://apify.com/radeance/similarweb-scraper)| [Tesco UK Scraper](https://apify.com/radeance/tesco-scraper)
|----------------------------|-----------------------------|-----------------------------|-----------------------------|

Welcome to this **Wellfound Job Listings Scraper** on **Apify**!<br><br>
This blazing fast & powerful tool is designed to effortlessly scrape job listings from Wellfound. Perfect for job seekers, recruiters, and market analysts, it can **scrape any job listing** on the site including information like **job title, description, job type, salary range, skills needed,** and much more. It also scrapes the job details page and provides comprehensive **company details like location, company website, company type, size, category, and badges**.

One of its best features is it's accuary & efficiency while scraping 1000s of jobs **in minutes** 💎
<br>

### [Try it today for free with our 3-day free trial! ](https://apify.com/radeance/wellfound-job-listings-scraper)

## Key Features

-   **🔍 Job Listings Extraction:**

    -   Scrapes job listings from Wellfound with pagination
    -   Extracts detailed information from job posting pages **automatically**
    -   Provides key details such as job id, title, description, posted_at, expires_at, salary range, skills, application url, and many many more.

-   **🏢 Company Information:**

    -   Scrapes company details including location, type, size, category, Website URL, LinkedIn, Facebook, Twitter and many more.

-   **⚡ Fast and Efficient:**

    -   Optimized for quality and efficiency you can scrape 1000s of job posts in minutes

-   **🔧 Advanced Customization:**

    -   Allows setting a specific job listings URL and the number of pages to scrape
    -   Easy to configure search queries for tailored results

-   **📊 Flexible Data Output:**
    -   Outputs data in various formats including CSV, XLSX, JSON, JSONL, XML, and RSS

### 🗂️ Use Cases | What it can be used for

-   **Recruiters & Hiring Managers**: To gather detailed job listings, including job title, location, pay range, and application and social media URLs.
-   **Job Seekers**: To find comprehensive job information, including job type, pay details, remote work policies, and company details.
-   **HR Analysts**: To analyze **market trends** in job postings, company sizes, and industry categories.
-   **Developers**: To integrate job listing data into applications for better job search experiences.

It streamlines the process of collecting and analyzing job market data, making it a valuable tool for various professionals.

### 📌 Input

![Scraper Sample Input](https://i.imgur.com/B1hq1tf.png)

-   `job_title`: (Optional) (String)
    Select desired job from the input list. If you can't find your desired job title use Custom Job Title input field. If you use a url in **advanced options** this gets ignored.
-   `job_location`: (Optional) (String)
    Select desired job location from the input list. If you can't find your desired job location use Custom Job Location input field. If you use a url in **advanced options** this gets ignored.
    <br>
-   `custom_job_title`: (Optional) (String)
    Enter your desired job title (e.g. Big Data Analyst). **Please be aware** that **not every job title** is available. You should check that your desired job title is available on Wellfound.
    💡 If you use this Field the `job_title` Field above is ignored.
-   `custom_job_location`: (Optional) (String)
    Enter your desired job location (e.g. London). **Please be aware** that **not every job location** is available. You should check that your desired job location is available on Wellfound.
    <br>
-   `max_pages`: (Optional) (Number)
    If this is set it **scrapes the amount of pages set**, unless there are no more pages to scrape, In this case the scraper retrieves all the data it could find. **Default** is set to 3.
    <br>
    ⚠️ If `max_items` limit is rechead this is ignored. If you want 100 pages of data it is recommended to set `max_items`to a high number.
-   `last_x_days`: (Optional) (Number)
    Filters scraped jobs by the inputed days to retrieve. For example an input value of 1 retrieves the jobs from the last 24h. **Default** is set to 365.
    <br>
-   `max_items`: (Optional) (Number)
    Caps the maximum number of job listing results. **Default** is set to 500.
    <br>
    💡 If you use this Field the `job_location` Field above is ignored.
-   `fully_remote`: (Optional) (Boolean)
    If set to **True** the actor outputs only jobs with remote work policy 'Onsite or remote' and 'Remote only'. If set to **False** it will output all jobs.
-   `us_date_format`: (Optional) (Boolean)
    If set to **True** the actor outputs every date field to US datetime format. If set to **False** it uses standard international datetime format.

### 🎛️ Advanced Options

#### Supported Job Listings URL Formats

| Link                                                                                                     | Supported |
| -------------------------------------------------------------------------------------------------------- | --------- |
| [https://wellfound.com/role/l/data-analyst/new-york](https://wellfound.com/role/l/data-analyst/new-york) | ✅        |
| [https://wellfound.com/role/r/data-analyst](https://wellfound.com/role/r/data-analyst)                   | ✅        |
| [https://wellfound.com/location/los-angeles](https://wellfound.com/location/los-angeles)                 | ✅        |

![Scraper Sample Input](https://i.imgur.com/3QY6zk4.png)

-   `urls`: (Optional) (String)
    Set your desired Wellfound Listings URLs directly from this input
    Provide the **URLs in the formats of the table above only**
    <br>
    ⚠️ If this is set it **replaces** the **Job Title** and **Job Location** (+ both custom fields) search parameters and **scrapes only using this URL** instead.
-   `page_offset`: (Optional) (Number)
    If this is set it **offsets the starting page to scrape**.For an input value of 5 the scraper would start at page 5 until max pages parameter is reached. **Default** is set to 1.

    #### ✏️ JSON Input

    Sample JSON input if you use the apify api via CURL, Python, JS etc.
    ![Scraper Sample Input](https://i.imgur.com/nu9SLg2.png)

### 📎 Detailed Output Information

-   **Job Details:** Including job ID, title, location, pay range, job type, visa sponsorship, remote work policy, relocation policy, job listing posted date, validity period, direct application status, required experience, and a detailed job description. Additional fields like minimum and maximum salary, salary currency, and salary unit are also included.
-   **Company Information:** Details about the company, including name, size, badges, location, category, stage, profile URL, website URL, logo URL, Twitter URL, and LinkedIn URL.
-   **Job Posting URL:** Direct link to the job posting and application page.
-   **Job Benefits:** Description of job benefits offered.
-   **Skills:** List of required skills for the job.
-   **Hires Remotely:** Information on remote hiring and location requirements.
-   **Export Formats:** Data can be exported in CSV, XLSX, JSON, JSONL, XML, and RSS formats for easy integration and analysis.

#### Output Data Sample

```json
 {
    "job_id": "3220047-senior-data-engineer",
    "job_auto_posted": false,
    "job_listing_posted": "05/16/2025 10:38:11 PM",
    "job_published": "1 week ago",
    "job_title": "Senior Data Engineer",
    "job_location": [
      "Remote",
      "Santiago",
      "Santiago Metropolitan Region"
    ],
    "job_details": [
      "$40k – $120k • 0.01% – 0.05%",
      "Remote • Santiago",
      "4 years of exp",
      "Full Time"
    ],
    "job_type": "Full Time",
    "job_compensation": "$40k – $120k • 0.01% – 0.05%",
    "job_pay_range": "$40k – $120k",
    "job_min_pay": "$40k",
    "job_max_pay": "$120k",
    "job_min_salary": 40000,
    "job_max_salary": 120000,
    "job_salary_currency": "USD",
    "job_salary_unit": "YEAR",
    "job_remote": true,
    "job_remote_possible": "yes",
    "skills": [
      "Python",
      "SQL",
      "Scala"
    ],
    "job_experience": "4 years of exp",
    "required_experience_years": 4,
    "required_experience_months": 48,
    "visa_sponsorship": "Not Available",
    "job_location_requirement": "United States",
    "remote_work_policy": "Onsite or remote",
    "hires_remotely": true,
    "relocation": "Relocation Allowed",
    "hiring_contact": null,
    "hires_remotely_in": [
      "Boston",
      "Santiago",
      "Lima District",
      "São Paulo",
      "Bogota",
      "Mexico City",
      "Buenos Aires",
      "Santiago"
    ],
    "collaboration_hours": "9:00 AM - 6:00 PM",
    "preferred_timezones": [
      "Pacific Time",
      "Mountain Time",
      "Central Time",
      "Eastern Time",
      "Atlantic Time",
      "Azores",
      "Coordinated Universal Time",
      "Central European Time",
      "Eastern European Time"
    ],
    "job_description": "About Topsort\nAt Topsort, we believe in the mission of democratizing the secret technologies of the walled gardens and creating a privacy-first cookie-free world of clean advertising with modern tech, friendly products, and AI. ...",
    "job_short_description": null,
    "job_benefits": "Remote Friendly -  Healthcare benefits -  Equity benefits",
    "job_url": "https://wellfound.com/jobs/3220047-senior-data-engineer",
    "job_listing_valid_until": "07/25/2025 06:21:06 PM",
    "direct_application": true,
    "job_application_url": "https://wellfound.com/jobs/3220047-senior-data-engineer?autoOpenApplication=true",
    "company": {
      "name": "Topsort",
      "category": [
        "B2B",
        "Sales and Marketing",
        "Marketplaces",
        "Developer Tools",
        "Ecommerce"
      ],
      "type": "SaaS",
      "stage": [
        "Growth Stage"
      ],
      "totaly_raised": 28500000,
      "totaly_raised_formatted": "$28.5M",
      "location": "Boston",
      "size": "51-200",
      "open_positions": null,
      "badges": [
        "B2B",
        "Growth Stage",
        "Top Investors"
      ],
      "profile_url": "https://wellfound.com/company/topsort",
      "url": "https://www.topsort.com",
      "logo_url": "https://photos.wellfound.com/startups/i/8193078-12b8e677f8db53e13c80ebd157f5ba24-medium_jpg.jpg?buster=1720630181",
      "email": null,
      "blog_url": null,
      "twitter_url": null,
      "linkedin_url": null,
      "facebook_url": null,
      "productHunt_url": null
    }
  },
```

### ⚙️ While the scraper is running

During the run, the actor will output log messages letting you know what is going on at any point. Each message always contains specific information about the process including which url / page the actor is working on.

If you provide invalid inputs to the actor, it will immediately stop with a failure state and output log messages explaining what is wrong. If you are unsure what went wrong feel free to open up an issue in the issue tab.

## 🔗 Legality of web scraping and scraping of job listings

The **Wellfound Job Listings Scraper** is designed to ethically extract **only publicly available job data and company information**, and it **does not** scrape private user data such as personal email addresses or personal identifiers.

Our scrapers are ethical and do not extract any private user data, such as email addresses, gender, or location. They only extract what the user has chosen to share publicly. We therefore believe that our scrapers, when used for ethical purposes by Apify users, are safe. However, you should be aware that your results could contain personal data. Personal data is protected by the GDPR in the European Union and by other regulations around the world. You should not scrape personal data unless you have a legitimate reason to do so. If you're unsure whether your reason is legitimate, consult your lawyers. You can also read our [blog post](https://blog.apify.com/is-web-scraping-legal/) on the legality of web scraping

## 💬 Feedback and Support

**Your satisfaction** is **important** to us! Therefore we are constantly striving to enhance the performance of our Actors.

If you have any technical feedback or encounter any bugs with the Wellfound Job Listings Scraper, please create an issue in the Actor’s Issues tab on the Apify Console.

You can also contact us directly for custom integrations or project use cases at business@radeance.com.

Thank you and happy scraping!


### [Try it today for free with our 3-day free trial! ](https://apify.com/radeance/wellfound-job-listings-scraper)