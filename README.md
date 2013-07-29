
# Xcode Archiving script - Andrea Bizzotto bizz84@gmail.com

========

Script to archive an existing xcode project to a target location. The script checks for a post-build action that defines the $ARCHIVE_PATH as follows:
<code>
echo "ARCHIVE_PATH=\"$ARCHIVE_PATH\"" > $PROJECT_DIR/archive_paths.sh
</code>
If such post-build action does not exist or running it doesn't define the $ARCHIVE_PATH variable, the script tries to generate it programmatically by finding the latest build in the expected archiving folder that matches the specified target name and date.

<b>Rationale</b>

For projects with a multitude of targets, generating the ARCHIVE_PATH programmatically can be a more maintainable solution, 
compared to exporting the scheme for each target and adding a post-action build script.

<b>Source Code</b>

The repository comes with a test Xcode iOS project that can be used to test the archive script.


