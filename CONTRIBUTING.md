# Contribution Guide

Thank you for your interest in contributing to Web3 Grants! Your efforts help us maintain a valuable resource for the entire Web3 community.

## How to Contribute

### Prerequisites

- A GitHub account
- Basic knowledge of Git and JSON

### Using the JSON Schema

Before you start contributing, it's crucial to understand how to use the JSON schema for creating or updating grant program entries. Each entry should follow this structure:

```json
{
  "organization_name": "String: Name of the organization managing the grant program",
  "grant_program_name": "String: Name of the grant program (if different from organization name)",
  "grant_program_description": "String: Detailed description of the grant program",
  "max_grant_size": Number: Maximum grant size in USD,
  "average_grant_size": Number: Average grant size in USD,
  "grant_type": "String: Choose from 'Equity-free grants', 'Recoverable or Equity based Grants', 'Both Equity-free and Equity based grants', or 'Other'",
  "type_of_funds_granted": "String: Choose from 'Native Token Grants Only', 'Native Token or Stablecoin/Fiat Grants', or 'Stablecoin or Fiat Grants Only'",
  "project_types": ["Array of strings: Choose from available project types"],
  "deadline": "String: Application deadline in YYYY-MM-DD format",
  "other_requirements": "String: Any additional requirements or information",
  "where_to_apply": "String: URL where applicants can apply",
  "marketing_networking_technical_community_support": "String: Information about additional support provided",
  "additional_resources": "String: Information about additional resources for grantees",
  "grant_program_guide": "String: URL of the grant program guide",
  "further_funding_opportunities": "String: Description of further funding opportunities",
  "public_contact_email": "String: Public email for contacting the grant program",
}
```

## What information each field is looking for:

### Organization Name (organization_name)

Write the name of the organization managing the grant program. For example, "Ethereum Foundation", "Web3 Foundation", "Solana Foundation".

### Grant Program Name (grant_program_name)

Write the name of the grant program. If it's the same as the organization name, you can leave this blank.

### Grant Program Description (grant_program_description)

Provide a detailed description of the grant program. Explain what the program is, what it does, and how it works. This is the main information that readers will use to understand the grant program.

### Maximum Grant Size (max_grant_size)

Enter the maximum grant size offered by your program in USD. Use a number without any currency symbols or commas. For example: 250000 (Positive numbers only). Even if the grant program only offers grants in native token or other currencies, state the USD equivalent. There is an opportunity in the type_of_funds_granted field to specify the actual currency type(s) your program provides.

### Average Grant Size (average_grant_size)

Enter the average grant size offered by your program in USD. Use a number without any currency symbols or commas. For example: 250000 (Positive numbers only). Even if the grant program only offers grants in native token or other currencies, state the USD equivalent. There is an opportunity in the type_of_funds_granted field to specify the actual currency type(s) your program provides.

### Grant Type (grant_type)

Choose one of the following options:

- "Equity-free grants"
- "Recoverable or Equity based Grants"
- "Both Equity-free and Equity based grants"
- "Other"

### Type of Funds Granted (type_of_funds_granted)

Choose one of the following options:

- "Native Token Grants Only"
- "Native Token or Stablecoin/Fiat Grants"
- "Stablecoin or Fiat Grants Only"

### Project Types (project_types)

List the types of projects invited to apply for the grant. Use an array format with one or more of the following options as Strings:

- "Development (Idea or MVP Stage)"
- "Integration (Existing project w/ traction/users)"
- "Growth or GTM"
- "Marketing or Community Building"
- "Technical Content, Tutorials, and Education"
- "Non-Technical Content and Education"
- "NFTs and Digital Art"
- "Gaming"
- "Governance and DAOs"
- "Academic or R&D"
- "Other"

For example: ["Development (Idea or MVP Stage)", "Integration (Existing project w/ traction/users)", "Gaming"]

### Deadline (deadline)

Enter the application deadline in UTC date format (YYYY-MM-DD). For example: "2024-12-31"

### Other Requirements (other_requirements)

Describe any additional requirements or information about the grant program.

### Where to Apply (where_to_apply)

Provide a valid URL where applicants can apply for a grant. For example: "https://web3grants.fyi/apply"

### Marketing, Networking, Technical, Community Support (marketing_networking_technical_community_support)

Describe any additional support your grant program or ecosystem provides to grantees, such as marketing, networking, technical, or community support.

### Additional Resources (additional_resources)

List any additional resources or information provided by the grant program to grantees, such as tools, platforms, exclusive events, cloud credits, discounts on services, etc.

### Grant Program Guide (grant_program_guide)

Provide a valid URL for your grant program guide or help resource. For example "https://web3grants.fyi/grant-guide"

### Further Funding Opportunities (further_funding_opportunities)

Describe any further funding opportunities beyond the initial grant, such as ecosystem funds, accelerator programs, VC connections, etc...

### Public Contact Email (public_contact_email)

Provide a valid email address that the public can use to contact your grants program.

Key points to remember:

- Ensure all required fields are filled out.
- Use the correct data types (strings, numbers, arrays) for each field.
- For fields with predefined options, choose only from the available options.
- Provide detailed and accurate information in all fields. Wherever possible, verify the information with the grant provider or program manager.

### Steps to Contribute

1. **Fork the Repository**

   - Click the "Fork" button at the top-right corner of this repository to create your own copy.

2. **Clone Your Fork**

   ```
   git clone https://github.com/your-username/web3-grants.git
   cd web3-grants
   ```

3. **Create a New Branch**

   - It's good practice to create a new branch for each contribution.

   ```
   git checkout -b add-new-grant
   ```

4. **Edit the JSON File**

   - Open `web3-grant-program-listings.json` in a text editor.
   - **Adding a New Grant Program**:
     - Append your grant program information using the provided JSON schema.
     - Ensure you're adding the new entry at the end of the file, before the closing bracket.
   - **Updating an Existing Grant Program**:
     - Locate the relevant entry and make the necessary changes.
     - Be careful not to alter the structure of the JSON.

5. **Validate the JSON**

   - Ensure your JSON is valid using a tool like JSONLint.
   - Check that your entry adheres to the schema structure provided above.

6. **Commit Your Changes**

   ```
   git add web3-grant-program-listings.json
   git commit -m "Add [Grant Program Name]"
   ```

7. **Push to Your Fork**

   ```
   git push origin add-new-grant
   ```

8. **Create a Pull Request**

   - First, ensure your fork is up to date with the main repository:
     ```
     git remote add upstream https://github.com/original-owner/web3-grants.git
     git fetch upstream
     git checkout main
     git merge upstream/main
     git checkout add-new-grant
     git rebase main
     ```
   - Push your changes to your fork:
     ```
     git push -f origin add-new-grant
     ```
   - Navigate to your fork on GitHub.
   - Click on "Compare & pull request" button that appears at the top of your repository page.
   - Ensure the "base repository" is the original repository and "base" is set to "main".
   - Ensure the "head repository" is your fork and "compare" is set to "add-new-grant".
   - Provide a clear title and description for your pull request.
   - Click "Create pull request" to submit it for review.

9. **Respond to Feedback**
   - Be responsive to any review comments or requests for changes.
   - Make necessary adjustments and push updates to your branch:
     ```
     git add .
     git commit -m "Address review comments"
     git push origin add-new-grant
     ```

## Best Practices

- **Follow the Schema**: Adhere strictly to the JSON schema to maintain consistency.
- **Keep Information Accurate**: Double-check all details for accuracy.
- **Respect Formatting**: Use proper indentation and formatting for readability.
- **Read the Community Guidelines**: Ensure your contribution aligns with our Community Guidelines.

## Getting Help

- **Issues**: If you're unsure about something, feel free to open an issue.
- **Contact**: Reach out via email at contact@web3grants.org for direct assistance.

Your contributions make a difference! Thank you for helping [Web3 Grants](https://web3grants.fyi) grow the Web3 ecosystem.
