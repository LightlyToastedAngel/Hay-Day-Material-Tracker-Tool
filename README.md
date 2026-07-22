# Hay Day Material Tracker

A customizable, offline-friendly material tracker for organizing Hay Day items across multiple farms or storage accounts.

The tracker runs entirely in your browser and includes automatic totals, account-to-account transfers, customizable categories, local saving, and backup import/export.

> [!IMPORTANT]
> This is an unofficial fan-made tool. Accounts created in the tracker are only local labels for organizing materials. They are not connected to, authenticated with, or synchronized with Hay Day or Supercell in any way.

## Features

- Add, rename, and remove tracker accounts
- Add, rename, move, and remove materials
- Add, rename, reorder, and remove categories
- Safely move materials before deleting a used category
- Increase, decrease, or directly enter material quantities
- Automatically calculate totals across all accounts
- Transfer materials between accounts
- View every account and material in one overview table
- Save changes automatically in the browser
- Export and import JSON backups
- Responsive dark interface
- Works without a server after the page has loaded

## Use the tracker

Open the published GitHub Pages site in a modern browser.

### 1. Add an account

1. Select **Manage accounts**.
2. Enter a name such as `Main Farm` or `Storage 1`.
3. Select **Add account**.

The names are only used inside the tracker. They do not need to match a real Supercell ID or Hay Day farm name.

### 2. Update material quantities

Open a category tab and find the account you want to update.

- Select **+** to add one item.
- Select **−** to remove one item.
- Enter a number directly to replace the current quantity.

Totals update automatically.

### 3. Transfer materials

Use **Transfer materials between accounts** near the bottom of the page.

1. Choose the source account.
2. Choose the destination account.
3. Choose the material.
4. Enter the quantity.
5. Select **Transfer**.

The tracker prevents transfers that exceed the quantity available on the source account.

## Manage materials

Select **Manage materials** to:

- Add a new material
- Rename an existing material
- Move a material to another category
- Delete a material

Renaming or moving a material preserves its quantities.

Deleting a material removes it and its quantities from every account, so the tracker asks for confirmation first.

## Manage categories

Select **Manage categories** to:

- Add a category
- Rename a category
- Move categories up or down
- Delete a category

A category containing materials cannot simply disappear. Before it is deleted, its materials must be moved into another category. Their account quantities are preserved.

The final remaining category cannot be deleted.

## Saving and privacy

The tracker uses browser `localStorage`.

This means:

- Data stays in the browser on the current device.
- No tracker data is sent to a database or external account.
- Changes save automatically.
- Different browsers have separate saved data.
- Private/incognito windows may delete their data when closed.
- Clearing browser site data can erase the saved tracker.
- The tracker does not automatically synchronize between devices.

Export backups regularly if the data matters to you.

## Backups

### Export a backup

1. Select **Export backup**.
2. Save the downloaded `.json` file somewhere safe.

The backup contains:

- Accounts
- Categories
- Materials
- Quantities
- Category order

### Import a backup

1. Select **Import backup**.
2. Choose a previously exported `.json` file.
3. The tracker will replace its current data with the imported data.

Export the current data before importing another backup if you may want to restore it later.

## Reset the tracker

Select **Reset all data** to return the tracker to its original public setup.

This removes added accounts, custom categories, custom materials, and entered quantities. Export a backup first if needed.

## Run it locally

No installation is required.

1. Download `index.html`.
2. Open it in a modern browser.

Most features work directly from the local file. Browser storage for local files can behave differently between browsers, so hosting it through GitHub Pages is recommended for regular use.

## Publish with GitHub Pages

### Create the repository

1. Create a new repository on GitHub.
2. Add `index.html` to the root of the repository.
3. Add this `README.md`.
4. Commit and push the files.

Your repository should look like this:

```text
your-repository/
├── index.html
└── README.md
```

### Enable GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings**.
3. Open **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing `index.html`, normally `main`.
6. Select the `/ (root)` folder.
7. Save the settings.

GitHub will display the published website address after deployment.

## Updating the published tracker

1. Edit or replace `index.html`.
2. Commit the change.
3. Push it to the branch used by GitHub Pages.

GitHub Pages will publish the new version automatically.

Existing browser data normally remains available when the page is updated at the same website address. Changing the repository name, custom domain, or page address may cause the browser to treat it as a different site with separate local storage. Export a backup before making those changes.

## Project structure

The entire tracker is contained in one file:

```text
index.html
```

That file contains:

- **HTML** for the page structure
- **CSS** for the dark theme and responsive layout
- **JavaScript** for accounts, materials, categories, totals, transfers, saving, and backups

Keeping everything in one file makes the project easy to host, share, and modify.

## Browser support

The tracker is intended for current desktop and mobile versions of browsers such as:

- Chrome
- Edge
- Firefox
- Opera
- Safari

JavaScript and browser storage must be enabled.

## Limitations

- The tracker cannot read your Hay Day barn or silo automatically.
- It does not connect to Hay Day, Supercell ID, or Supercell servers.
- Data does not automatically synchronize across browsers or devices.
- Browser data may be lost if site storage is cleared without a backup.

## Disclaimer

This project is unofficial and is not affiliated with, endorsed by, sponsored by, or connected to Supercell. Hay Day and related names belong to their respective owners.
