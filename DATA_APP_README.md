# Data Storage and Retrieval App

A simple, user-friendly web application for storing and retrieving data using browser's localStorage.

## Features

### 📝 Store Data
- **Key-Value Storage**: Store data using unique keys
- **Flexible Data**: Store any text-based data (notes, configurations, JSON, etc.)
- **Update Support**: Update existing data by using the same key
- **Automatic Timestamps**: Each entry is timestamped automatically

### 🔍 Retrieve Data
- **View All Data**: Display all stored data items
- **Search Functionality**: Filter data by key name
- **Sorted Display**: Items are sorted by timestamp (newest first)
- **Rich Display**: Shows key, value, and timestamp for each item

### 🗑️ Delete Data
- **Individual Deletion**: Delete specific data items
- **Confirmation Prompt**: Prevents accidental deletions

### 📊 Statistics
- **Item Count**: Shows total number of stored items
- **Storage Usage**: Displays approximate storage space used

## How to Use

### Accessing the App
1. Navigate to `/data-app/` on the website
2. The app loads automatically with any previously stored data

### Storing Data
1. Enter a unique **Key** (identifier) for your data
2. Enter the **Value** (the actual data you want to store)
3. Click **"Save Data"** button
4. You'll see a success message confirming the save

### Retrieving Data
- All stored data is automatically displayed in the "Retrieve Data" section
- Use the search box to filter items by key name
- Each item shows:
  - The key (identifier)
  - The stored value
  - The timestamp when it was saved

### Deleting Data
1. Find the item you want to delete in the "Retrieve Data" section
2. Click the **"Delete"** button next to the item
3. Confirm the deletion when prompted

### Updating Data
- To update an existing item, simply enter the same key with a new value
- The app will update the existing entry instead of creating a duplicate

## Technical Details

### Storage Mechanism
- Uses **localStorage** API for client-side data persistence
- Data persists across browser sessions
- Storage limit: Typically 5-10MB depending on browser

### Data Format
Each stored item includes:
```json
{
  "key": "unique-identifier",
  "value": "your-data",
  "timestamp": "2025-11-28T03:04:57.982Z",
  "lastModified": "2025-11-28T03:04:57.982Z"
}
```

### Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Requires JavaScript enabled
- localStorage support required

### Security Considerations
- Data is stored locally in the browser
- Not suitable for sensitive/confidential information
- Data is not encrypted
- Accessible only from the same domain
- XSS protection through HTML escaping

## Use Cases

- **Quick Notes**: Store temporary notes or reminders
- **Configuration Storage**: Save user preferences or settings
- **Draft Storage**: Keep draft content before submission
- **Testing**: Test data storage mechanisms
- **Learning**: Understand how localStorage works

## Limitations

1. **Browser-Specific**: Data is stored per browser and device
2. **No Synchronization**: Data doesn't sync across devices
3. **Storage Limit**: Subject to browser's localStorage limits
4. **No Server Backup**: Data exists only in the browser
5. **Clearable**: Can be cleared by browser cache/data clearing

## Integration with Jekyll Site

The app is integrated as a Jekyll page:
- Located at: `_pages/data-app.html`
- Accessible via: `/data-app/` URL
- Uses Jekyll's `single` layout
- Includes author profile

## Future Enhancements

Possible improvements:
- Export/Import functionality
- Data validation
- Rich text editor
- Data encryption
- Cloud synchronization
- Mobile app version
- Bulk operations
- Data categorization/tagging

## Troubleshooting

### Data Not Saving
- Check if localStorage is enabled in your browser
- Verify you're not in private/incognito mode (limited storage)
- Check if storage quota is exceeded

### Data Lost
- localStorage data can be cleared by:
  - Clearing browser cache/data
  - Browser updates
  - Using private browsing mode

### App Not Loading
- Ensure JavaScript is enabled
- Check browser console for errors
- Try refreshing the page

## Support

For issues or questions, please create an issue on the GitHub repository.

## License

This app is part of the website repository and follows the same license terms.
