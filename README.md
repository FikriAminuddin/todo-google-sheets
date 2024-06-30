# Google Sheets Integration

This project demonstrates how to integrate a Google Sheet into a React project using Apico.

## Getting Started

These instructions will guide you through the setup and usage of the project.

### Prerequisites

Ensure you have the following installed:

- Node.js
- npm (Node Package Manager)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/FikriAminuddin/todo-google-sheets.git
   cd todo-google-sheets
   ```

2. **Install the dependencies:**
   ```bash
   npm install
   ```

### Configuration

1. **Create a Google Sheet Integration in Apico:**
   - Login to your [Apico](https://apico.dev/) account.
   - Create a new Google Sheets integration.
   - Note the integration ID and keep it handy for the next step.

![Apico API Example Screenshot](/docs/Screenshot-API.png)

2. **Create an Empty Google Sheet in Your Google Account:**
   - Login to your [Google Sheets](https://sheets.google.com/) account.
   - Create a new Google Sheet.
   - Note down the URL. It should look something like this:
     ```
     https://docs.google.com/spreadsheets/d/1GF_fQYoFODJITUbZapaQA_bIHKtgWpg5Gd56ENd-9Gs/edit#gid=0
     ```

3. **Get the Required Variables from the URL:**
   - `spreadSheetId`: `1GF_fQYoFODJITUbZapaQA_bIHKtgWpg5Gd56ENd-9Gs`
   - `sheetId`: `0` (or as displayed in the URL)
   - `sheetName`: (Assuming it is the default name, "Sheet1"; if different, replace with the actual name)

4. **Replace the Variables in the Code:**
   - Open the `/src/api/sheets.ts` file.
   - Replace the placeholder values with your actual values:
     ```typescript
     const apicoIntegrationId: string = "<Your apico gsheet integration id>";
     const spreadSheetId: string = "1GF_fQYoFODJITUbZapaQA_bIHKtgWpg5Gd56ENd-9Gs";
     const sheetName: string = "Sheet1"; // replace with your sheet name if different
     const sheetId: number = 0; // the gid from your URL
     ```

### Running the Project

To run the project, use the following command:

```bash
npm run dev
```

### Troubleshooting

If you encounter any issues, ensure that:

- Your Google Sheets API is enabled and properly configured.
- The Apico GSheet integration ID is correct.
- The Google Sheet ID and sheet ID are accurate.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. For significant changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Google Sheets API Documentation](https://developers.google.com/sheets/api)
- [Apico Integration Documentation](https://apico.com/docs)

---

Feel free to customize this README file further to suit your project's needs.