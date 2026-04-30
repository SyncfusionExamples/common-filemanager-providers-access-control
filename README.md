# Common-filemanager-providers-access-control

**Repository Description**  
This repository contains the **ASP.NET Core file system providers** for the Syncfusion **Essential JS 2 File Manager** component. These providers expose server‑side APIs that allow the File Manager UI to interact with the physical file system for common file operations.

The ASP.NET Core file system provider enables secure access to directories and supports a wide range of file management actions required by the File Manager component.

## Project Overview
The purpose of this project is to provide a backend implementation for the Syncfusion Essential JS 2 File Manager component using **ASP.NET Core**. It demonstrates how to handle file system operations such as reading files, uploading content, renaming items, and managing folders through REST‑style APIs.

## Prerequisites
Ensure the following requirements are met before running this project:
- Visual Studio  
- .NET SDK compatible with ASP.NET Core  
- Basic knowledge of ASP.NET Core Web APIs  

## Key Features

A file system provider is an API for access to the physical file system in the FileManager control. It also provides the methods for performing various file actions like creating a new folder, renaming files and deleting files.

ASP.NET Core file system provider serves the physical file system for the file manager component.

The following actions can be performed with ASP.NET Core file system Provider.

| **Action**  | **Description** |
|------------|------------------|
| Read       | Reads files from the local file storage. |
| Details    | Retrieves file metadata, including **Type**, **Size**, **Location**, and **Modified Date**. |
| Download   | Downloads the selected file or folder. |
| Upload     | Uploads files with the following constraints:<br><ul><li>Maximum file size: **30 MB**</li><li>Accepted MIME types: `*/*`</li></ul> |
| Create     | Creates a new folder. |
| Delete     | Deletes a file or folder. |
| Copy       | Copies files or folders from the source location. |
| Move       | Moves (pastes) copied files or folders to the target location. |
| Rename     | Renames a file or folder. |
| Search     | Searches for files or folders. |

## Installation and Running the Project

### How to run this application?

To run this application, you need to first clone the `ej2-aspcore-file-provider` repository and then navigate to its appropriate path where it has been located in your system.

To do so, open the command prompt and run the below commands one after the other.

```
git clone https://github.com/SyncfusionExamples/ej2-aspcore-file-provider  ej2-aspcore-file-provider

cd ej2-aspcore-file-provider

```

### Running application

Once cloned, open solution file in visual studio.Then build the project after restoring the nuget packages and run it.

### File Manager AjaxSettings

To access the basic actions such as Read, Delete, Copy, Move, Rename, Search, and Get Details of File Manager using Azure service, just map the following code snippet in the Ajaxsettings property of File Manager.

Here, the `hostUrl` will be your locally hosted port number.

```
  var hostUrl = http://localhost:62870/;
  ajaxSettings: {
        url: hostUrl + 'api/FileManager/FileOperations'
  }
```

### File download AjaxSettings

To perform download operation, initialize the `downloadUrl` property in ajaxSettings of the File Manager component.

```
  var hostUrl = http://localhost:62870/;
  ajaxSettings: {
        url: hostUrl + 'api/FileManager/FileOperations',
        downloadUrl: hostUrl +'api/FileManager/Download'
  }
```

### File upload AjaxSettings

To perform upload operation, initialize the `uploadUrl` property in ajaxSettings of the File Manager component.

```
  var hostUrl = http://localhost:62870/;
  ajaxSettings: {
        url: hostUrl + 'api/FileManager/FileOperations',
        uploadUrl: hostUrl +'api/FileManager/Upload'
  }
```

### File image preview AjaxSettings

To perform image preview support in the File Manager component, initialize the `getImageUrl` property in ajaxSettings of the File Manager component.

```
  var hostUrl = http://localhost:62870/;
  ajaxSettings: {
        url: hostUrl + 'api/FileManager/FileOperations',
         getImageUrl: hostUrl +'api/FileManager/GetImage'
  }
```

The FileManager will be rendered as the following.

![File Manager](https://ej2.syncfusion.com/products/images/file-manager/readme.gif)

## Documentation
- General Syncfusion documentation:
https://help.syncfusion.com/
- Essential JS 2 File Manager – Getting Started:
https://ej2.syncfusion.com/documentation/file-manager/

## Additional Resources
- Syncfusion File Manager product overview:
https://www.syncfusion.com/javascript-ui-controls/js-file-manager

## Troubleshooting
- Ensure the API URLs in ajaxSettings match the running server port.
- Verify file system permissions for read/write operations.
- Rebuild the solution if API endpoints fail to respond.

## Support

Product support is available for through following mediums.

* Creating incident in Syncfusion [Direct-trac](https://www.syncfusion.com/support/directtrac/incidents?utm_source=npm&utm_campaign=filemanager) support system or [Community forum](https://www.syncfusion.com/forums/essential-js2?utm_source=npm&utm_campaign=filemanager).
* New [GitHub issue](https://github.com/syncfusion/ej2-javascript-ui-controls/issues/new).
* Ask your query in [Stack Overflow](https://stackoverflow.com/?utm_source=npm&utm_campaign=filemanager) with tag `syncfusion` and `ej2`.

## License

Check the license detail [here](https://github.com/syncfusion/ej2-javascript-ui-controls/blob/master/license).

## Changelog

Check the changelog [here](https://github.com/syncfusion/ej2-javascript-ui-controls/blob/master/controls/filemanager/CHANGELOG.md)

© Copyright 2019 Syncfusion, Inc. All Rights Reserved. The Syncfusion Essential Studio license and copyright applies to this distribution.