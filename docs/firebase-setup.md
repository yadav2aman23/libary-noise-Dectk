# Firebase Setup

These are general setup steps. Follow the exact configuration expected by your firmware and installed Firebase library.

1. Create a project in the Firebase Console.
2. Create or enable a Realtime Database.
3. Configure the authentication method required by your firmware.
4. Set secure Realtime Database Security Rules. Avoid public read/write access for a real deployment.
5. Add the required database URL and credentials to your local firmware configuration.
6. Connect the ESP32 to Wi-Fi and upload the sketch.
7. Use Serial Monitor to check connection and write errors.
8. Confirm that the expected data path and fields appear in the Realtime Database console.

## Security checklist

- Never commit Wi-Fi passwords, access tokens, private keys, service-account JSON, or other secrets.
- Use placeholders in screenshots and examples.
- If credentials were committed by mistake, remove them from the repository and rotate/revoke them; deleting the latest copy alone may not remove them from Git history.
- Use the least-privilege database rules appropriate for the project.

## Troubleshooting

- Check that the ESP32 has a working Wi-Fi connection.
- Verify the database URL and configured authentication method.
- Review Firebase library documentation for the version used by your sketch.
- Check Serial Monitor output for the specific error.
- Verify that the firmware is writing to the path you are inspecting.
