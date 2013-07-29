
#### Xcode Archiving script - Andrea Bizzotto bizz84@gmail.com

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

<b>License</b>

Copyright (c) 2013 Andrea Bizzotto bizz84@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
