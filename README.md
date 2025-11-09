# Facility Booking Web App

A responsive, dark-themed facility booking web application that works completely offline without any backend server.

## Features

- ✨ Modern dark theme UI
- 📱 Fully responsive design
- 📅 Interactive calendar date picker
- 🕐 Time slot selection
- 🔍 Real-time search functionality
- 🖼️ Booking confirmation with downloadable PNG
- 🎨 Customizable facilities via JSON

## Getting Started

1. Simply open `index.html` in your web browser
2. No server or installation required!

## How to Use

### Booking a Facility

1. **Browse Facilities**: View all available facilities on the home page
2. **Search**: Use the search box to filter facilities by name
3. **Select Facility**: Click on any facility card to view details
4. **Choose Date**: Click the date field to open the calendar and select a date
5. **Choose Time**: Click the time field to select a time slot (7 AM - 11 PM)
6. **Add Remarks**: Optionally add any remarks
7. **Confirm**: Click "Confirm Booking" to finalize
8. **Download**: Download your booking confirmation as a PNG image

## Customization

### Adding Real Images

To use real facility images instead of placeholders:

1. Place your images in an `images/` folder
2. Edit `facilities.json` to update the image paths:

```json
{
    "id": 1,
    "name": "AEROBIC",
    "image": "images/aerobic-header.jpg",
    "templateImage": "images/aerobic-template.jpg",
    ...
}
```

### Facility Data Structure

Each facility in `facilities.json` has the following properties:

- `id`: Unique identifier
- `name`: Facility name displayed on the card and detail page
- `image`: Header image shown in the list and detail page
- `templateImage`: Template image used for booking confirmation
- `status`: Status text (e.g., "Approval Required*")
- `description`: Detailed description of the facility, rules, and operation hours

### Modifying Time Slots

Edit the `timeSlots` array in the HTML file (around line 433):

```javascript
const timeSlots = [
    "7:00 AM - 9:00 AM", 
    "9:00 AM - 11:00 AM", 
    // Add more slots here
];
```

## Browser Compatibility

Works on all modern browsers:
- Chrome / Edge (recommended)
- Firefox
- Safari
- Opera

## Technical Details

- **Pure Frontend**: HTML5 + CSS3 + Vanilla JavaScript
- **No Dependencies**: No external libraries required
- **Canvas API**: Used for generating booking confirmation images
- **Responsive**: Mobile-first design with breakpoints
- **Local Storage Ready**: Can be extended to save bookings locally

## File Structure

```
├── index.html          # Main application file
├── facilities.json     # Facility data (for reference)
└── README.md          # This file
```

## Tips

- The app defaults to today's date and current time slot
- Past dates are disabled in the calendar
- Booking confirmations include a unique booking ID
- Images can be Data URIs or file paths (for local files)

## Future Enhancements

Potential features you can add:
- Local Storage for saving bookings
- Multiple facility booking in one session
- User profile management
- Booking history
- Email confirmation (requires backend)
- Payment integration (requires backend)

---

**Note**: This app works completely offline. All data is handled client-side. To use custom images, ensure they are accessible via the file path or use Data URIs.

