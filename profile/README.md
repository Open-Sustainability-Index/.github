# Open Sustainability Index

_Open, accessible, transparent, actionable sustainability data._

We believe in open data and open source.

## Do you want to help building Open Sustainability Index?

- Read our [Introduction for new contributors](https://github.com/orgs/Open-Sustainability-Index/discussions/12) in the discussions.
  - Read [how to set up your development environment](https://github.com/Open-Sustainability-Index/open-sustainability-index-frontend?tab=readme-ov-file#how-to-set-up)
  - We have a development todo list here: https://github.com/orgs/Open-Sustainability-Index/projects/1/views/3 but feel free to come up with your own ideas too!
  - See https://www.opensustainabilityindex.org/support-us for more information on how to contribute to Open Sustainability Index.
- See https://www.opensustainabilityindex.org/api on how to access the data through our API.

## Development workflow

- Always work in separate branches, and use pull requests.
- Process:
	1. When starting on new task, assign yourself to the [GitHub task card](https://github.com/orgs/Open-Sustainability-Index/projects/1/views/3) and move the card to “In Progress” lane.
	2. Create new branch for new feature: `dev/[description-of-feature]` (PR title: “Description of feature”) or fix: `dev/fix-[description-of-bug]` (PR title: “Description of bug”).
	3. Apply code linting/prettifier – `npm run fix` – before committing code and correct any issues.
	4. Create [pull request (PR)](https://github.com/Open-Sustainability-Index/open-sustainability-index-frontend/pulls) on GitHub.
	5. Tech Lead will approve pull request and merge into `main` branch.
- It’s ok to merge `main` branch into your feature branch to solve conflicts.
- Versioning (in `package.json`) done by Tech Lead: `v1.2.3` = `v[Major].[Minor].[Patch]`. Minor: when a new screen/page is added, Patch for other changes.

## Submit new emission data
If you have a csv with emission data you can submit it to Supabase following these steps:
1. Go to the [emission table](https://supabase.com/dashboard/project/xtvsbqwnsdqzjdqirdha/editor/29915?schema=public)
2. Click "Insert"
3. Click "Import data from CSV"
4. Click "Paste text"
5. Paste the contents of your CSV file into the text box
6. Click "Insert". DONE!

If The above resulted in this error:
```
Failed to import data: insert or update on table "emission" violates foreign key constraint "public_emission_slug_fkey"
```
It means the company does not yet exist in the database. To add it manually you can do:
1. Go to the [company table](https://supabase.com/dashboard/project/xtvsbqwnsdqzjdqirdha/editor/29925?schema=public)
2. Click "Insert"
3. Click "Insert row"
4. Fill in the 2 necessary rows (name, slug). Name should be the name of the company. Slug is the unique identifier for this company. It could be anything, but normally it's a computer friendly version of the name. Replace spaces in the name with `-` and replace language specific characters such as `åäö`. Make it lower-case. A good slug for `Diös Fastigheter` would for example be `dios-fastigheter`
5. Click "Save"
6. The company is now saved and you can add the column `company_slug` to your csv with the slug of the company you just added and redo the emission steps [above](https://github.com/Open-Sustainability-Index/.github/edit/main/profile/README.md#submit-new-emission-data). 

## Communication

We use [GitHub Discussions](https://github.com/orgs/Open-Sustainability-Index/discussions) for communications around development and design of Open Sustainability Index.

Send an email to hello@opensustainabilityindex.org if you have other questions.
