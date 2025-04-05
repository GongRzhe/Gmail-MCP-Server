# Add Label Management Functionality

## Overview
This PR adds comprehensive label management functionality to the Gmail MCP Server, allowing users to create, update, delete, and list labels directly through Claude.

## Features Added
- **Create Label**: Create new Gmail labels with configurable visibility settings
- **Update Label**: Modify existing labels' names and visibility settings
- **Delete Label**: Remove user-created labels with appropriate safeguards for system labels
- **Get or Create Label**: Fetch a label by name or create it if not found
- **Enhanced Label Listing**: Improved label listing with better organization and details

## Implementation Details
- Added new `label-manager.ts` module with core label management functions
- Added schema definitions for the new label operations
- Extended index.ts to include new tool handlers for label operations
- Updated README.md to document the new features
- Follows the same coding style and patterns as the existing codebase
- Added comprehensive error handling and user-friendly error messages

## Testing
All functions have been tested with the Gmail API to ensure they work correctly:
- Creating labels with various visibility settings
- Updating existing labels
- Attempting to delete system labels (correctly prevented)
- Deleting user labels
- Finding labels by name
- Getting or creating labels

## Use Cases
This enhancement makes it much easier for users to organize their emails through Claude without needing to switch to the Gmail interface. Examples include:
- Creating a structured label system for project emails
- Auto-organizing emails with custom labels
- Cleaning up and reorganizing existing labels
- Creating labels on-the-fly during email organization workflows

## Documentation
The README has been updated to include:
- New feature descriptions
- Detailed documentation for each new tool
- Examples of how to use each label management function
- Information about label visibility options

This PR builds on the foundation of the batch operations PR I contributed earlier, continuing to enhance the functionality and usability of the Gmail MCP Server.