# Restaurant Finder App

This application shows all types of restaurants near your location using Google Maps.

## IMPORTANT: API Key Setup

The app requires a valid Google Maps API key to function correctly. Follow these steps to set up your own API key:

1. Obtain a Google Maps API Key:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/).
   - Create a new project or select an existing one.
   - Enable the following APIs:
     - Maps JavaScript API
     - Places API
   - Create credentials (API key) for these APIs.
   - Restrict the API key to your domain for security.

2. Set up the environment variable:
   - Open the `.env` file in the root of the project.
   - Replace `REPLACE_WITH_YOUR_ACTUAL_API_KEY` with your Google Maps API key:
     ```
     VITE_GOOGLE_MAPS_API_KEY=your_actual_api_key_here
     ```
   - Save the file.

3. Restart the development server:
   - Stop the current server (if running) by pressing Ctrl+C in the terminal.
   - Run the server again with:
     ```
     npm run dev
     ```

## Running the Application

After setting up your API key, follow these steps to run the application:

1. Install dependencies (if you haven't already):
   ```
   npm install
   ```

2. Run the development server:
   ```
   npm run dev
   ```

3. Open the application in your browser at the URL provided by Vite.

## Troubleshooting

### Google Maps JavaScript API error: InvalidKeyMapError

If you see this error, it means the app is using an invalid or placeholder API key. To fix this:

1. Check that you've replaced `REPLACE_WITH_YOUR_ACTUAL_API_KEY` in the `.env` file with your actual Google Maps API key.
2. Ensure that your API key has the necessary permissions (Maps JavaScript API and Places API) enabled in the Google Cloud Console.
3. Verify that you've saved the `.env` file after making changes.
4. Restart the development server after updating the `.env` file:
   ```
   npm run dev
   ```

If you continue to see this error after following these steps, double-check your API key in the Google Cloud Console and ensure it's correctly copied into the `.env` file.

For additional troubleshooting, review the [Google Maps JavaScript API documentation](https://developers.google.com/maps/documentation/javascript/overview).

Remember: Never commit your actual API key to version control. The `.env` file should be listed in your `.gitignore` file to prevent accidental commits.