### Overview:
The task involves building an Event Planning App with the following key features:

1. **Events List Page:**
   - Displays a list of upcoming events with essential details.
   - Includes a [Create Event] button at the top.
   - Each event card includes [View Guests], [Edit], and [Create Guest] buttons.

2. **Event Guest List Page:**
   - Displays detailed information about a specific event.
   - Lists guests with their names, email addresses, RSVP status, and optional comments.
   - Includes [Edit Event] and [Create Guest] buttons.

3. **Create/Edit Event Form:**
   - A form for creating a new event or editing an existing one.
   - Input fields include event name, date, time, location, description, and category.
   - [Save] Button for submission.

4. **Create/Edit Guest Form:**
   - A form for creating a new guest or editing an existing one for a specific event.
   - Input fields include guest name, email, RSVP status, and optional comments.
   - [Save] Button for submission.

### Page Contents:

#### 1. Events List Page:

**Components:**
- **EventCard:**
  - Displays a card for each event.
  - Shows key details such as event name, date, time, and location.
  - Provides buttons for [View Guests], [Edit], and [Create Guest].

**UI Structure:**
```plaintext
Events List Page
  - [Create Event] Button

  - EventCard 1
    - Event Name: Birthday Party
    - Date: 2023-12-31
    - Time: 18:00:00
    - Location: 123 Main Street
    - [View Guests] Button
    - [Edit] Button
    - [Create Guest] Button

  - EventCard 2
    - Event Name: Conference
    - Date: 2024-01-15
    - Time: 09:00:00
    - Location: Convention Center
    - [View Guests] Button
    - [Edit Event] Button
    - [Create Guest] Button
  - ...
```

**JSON Format:**
```json
{
  "events": [
    {
      "id": 1,
      "name": "Birthday Party",
      "date": "2023-12-31",
      "time": "18:00:00",
      "location": "123 Main Street",
      "description": "Join us for a fun birthday celebration!",
      "category": "Celebration",
      "guests": [
        {
          "id": 101,
          "name": "John Doe",
          "email": "john.doe@example.com",
          "rsvp": "Attending",
          "comments": "Looking forward to it!"
        },
        // Additional guests...
      ]
    },
    // Additional events...
  ]
}
```

#### 2. Event Guest List Page:

**Components:**
- **GuestCard:**
  - Displays a card for each guest.
  - Shows guest name, email, RSVP status, and optional comments.
  - Includes [Edit Event] and [Create Guest] buttons.

**UI Structure:**
```plaintext
Event Guest List Page
  Event Details
    - Event Name: Birthday Party
    - Date: 2023-12-31
    - Time: 18:00:00
    - Location: 123 Main Street
    - [Edit Event] Button
    - [Create Guest] Button

  - Guest Card 1
    - Guest Name: John Doe
    - Email: john.doe@example.com
    - RSVP: Attending
    - Comments: Looking forward to it!
    - [Edit Guest] Button

  - Guest Card 2
    - Guest Name: Jane Smith
    - Email: jane.smith@example.com
    - RSVP: Not Attending
    - Comments: Sorry, I have another commitment.
    - [Edit Guest] Button
  - ...
```

**JSON Format:**
```json
{
  "events": [
    {
      "id": 1,
      "name": "Birthday Party",
      "date": "2023-12-31",
      "time": "18:00:00",
      "location": "123 Main Street",
      "guests": [
        {
          "id": 101,
          "name": "John Doe",
          "email": "john.doe@example.com",
          "rsvp": "Attending",
          "comments": "Looking forward to it!"
        },
        // Additional guests...
      ]
    },
    // Additional events...
  ]
}
```

#### 3. Create/Edit Event Form:

**Components:**
- **EventForm:**
  - A form for creating or editing an event.
  - Input fields include event name, date, time, location, description, and category.
  - [Save] Button for submission.

**UI Structure:**
```plaintext
- Create/Edit Event Form
  - Event Name Input
  - Date Input
  - Time Input
  - Location Input
  - Description Input
  - Category Input
  - [Save] Button
```

**JSON Format:**
```json
{
  "name": "Birthday Party",
  "date": "2023-12-31",
  "time": "18:00:00",
  "location": "123 Main Street",
  "description": "Join us for a fun birthday celebration!",
  "category": "Celebration"
}
```

#### 4. Create/Edit Guest Form:

**Components:**
- **GuestForm:**
  - A form for creating or editing a guest for a specific event.
  - Input fields include guest name, email, RSVP status, and optional comments.
  - [Save] Button for submission.

**UI Structure:**
```plaintext
- Create/Edit Guest Form
  - Guest Name Input
  - Email Input
  - RSVP Status Dropdown (Attending, Not Attending, Pending)
  - Comments Input (Optional)
  - [Save] Button
```

**JSON Format:**
```json
{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "rsvp": "Attending",
  "comments": "Looking forward to it!"
}
```
### Storing Events data
Let's store the inputted data json in the localStorage to persist the details on page reload for various events and corresponding guests.
