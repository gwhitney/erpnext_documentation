[Setting Up](/docs/user/manual/en/setting-up) > Chart Importer
# Chart Importer

> Introduced in Version 12

When a new company is created in ERPNext, the Chart of Accounts for it is created by default with a pre-set structure, and it receives a minimal Chart of Cost Centers consisting of just a single main Cost Center. However, if you have your own Chart of Accounts and/or Chart of Cost Centers, you can import them using the Chart Importer. An important caveat, though: you can only do this *before* you have created any transactions for your company.

It allows you to create your own Chart of Accounts or of Cost Centers according to your particular requirements and import it into the system.

Any existing Chart Of Accounts/Chart of Cost Centers against that company will be overwritten. Make sure the company you are selecting doesn't have any pre-existing transactions otherwise you'll receive a validation error.

To access, go to:
> Home > Data Import and Settings > Chart Importer

## 1. How to import a Chart

1. Select the Company for which you want to import the Chart of Accounts or Chart of Cost Centers, and then select which type of chart you wish to create.

1. Click on the "Download Template" button to download the template. Select the file type in which you want to download the template. Select the template type and click on "Download". "Sample Template" contains pre-filled sample data so that you get an idea of how to fill the template. You can edit the data in "Sample Template" itself or download "Blank Template" for a fresh template. [NOTE: Both screen shots below need updating.]

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-template-download.png">

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-blank-template.png">

1. Once you download the template, fill in the details in the template. An example for the Chart Of Accounts is given sample template below. Please make sure to make accounts for account types "Cost of Goods Sold", "Depreciation", "Fixed Asset", "Payable", "Receivable", "Stock Adjustment". Root types for these accounts must be one of Asset, Liability, Income, Expense, and Equity. 

    To learn more about "Account Types" and "Root Types" <a href="/docs/user/manual/en/accounts/chart-of-accounts">click here</a>.

    For both types of Charts, assignment of numbers to your entries is optional; you may use numbers if it aids your organization's accounting practices, and you may tailor them as you see fit (they are not actually even required to be strictly numeric). You should set the "Is Group" field to 0 for entries you want to actually assign to individual transactions; other entries can be used for headings that accumulate these basic ones, and should be assigned 1 in the "Is Group" field.

    For the Chart of Cost Centers, the only fields that require further explanation are the ones associated with "Distributed Cost Centers." These can be used to allocate expenses, such as rent or security costs, that cut across your other categorizations. So most Cost Centers will have "Enable Distributed Cost Center" equal to 0. For one that you do want to use to allocate expenses, set "Enable Distributed Cost Center" to 1, and then put the name of the first Cost Center to distribute to on that same line in the "Cost Center (Distributed Cost Center" field, and the percentage of these charges that go to that Cost Center in the "Percentage Allocation (Distributed Cost Center)" field. Then in the *immediately succeeding* lines of your spreadsheet, fill in the other Cost Centers to distribute to and their allocations. Put one destination for the distribution on each line, and fill in *only* these two fields on successive lines. The sum of all of the percent allocations for one distributing Cost Center must be 100. After all of the allocation lines, you simply continue with the next, unrelated primary Cost Center in the usual way, using all the normal fields. The "Sample Template" which you can download shows a couple of examples of this.

    And here's that example Chart of Accounts spreadsheet, ready for importing.[NOTE: The sample COA screenshot below needs updating.]

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-sample-template.png">

1. Click on "Attach" to upload the template. [NOTE: screen shot needs updating]

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-attach.png">

1. Once you upload the template, but before you actually perform the import which alters your database, you'll be able to see the Chart Preview section. Here's an example from a Chart of Cost Centers import in progress: [NOTE: Replace screen shot with one from a Chart of Cost Centers.]

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-preview.png">

1. If everything seems correct in the preview, click on the "Import" button in the top right corner and the accounts will be created.


1. To verify the created Accounts and/or Cost Centers you can go to Chart of Accounts or Chart of Cost Centers and see the newly created records for that company. [NOTE: Add a screenshot for Chart of Cost Centers.]

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-import.png">

1. If anything seems amiss, note that you can go back to the Chart Importer and re-load a modified file, completely replacing everything you just did. You can do this any number of times until your Accounts and/or Cost Centers come out right -- up until you add your first actual transaction to your company's ledger, at which time the Chart Importer will no longer operate for that company (but it will work for any other new companies you add, before they have transactions).

### 2. Related Topics
1. [Chart Of Accounts](/docs/user/manual/en/accounts/chart-of-accounts)

1. [Cost Centers](/docs/user/manual/en/accounts/cost-center)

