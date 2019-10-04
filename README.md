# manifest-overwrite-bug
an example of the manifest overwrite bug for flywheel

To replicate this bug:
1. Ensure you have flywheel CLI installed on your machine
2. Clone this repository
3. Enter the repository's directory and type ` fw gear create `
4. Enter appropriate names and ID's for the gear (These we expect to overwrite, and are not considered a bug)
5. Choose any base image (The Dockerfile and gear manifest specify `dbp2123/manifest-bug:1.0`, but for this test it's not critical)
6. Choose "Analysis" or "Converter" (Not critical)

Now compare the new manifest.json file with the original-manifest.json file, paying close attention to the "version" and "custom" fields.

