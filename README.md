# 📚 StudentFocus - Ultimate Study Manager

A comprehensive, feature-rich study management app for students with task tracking, Pomodoro timer, grade calculator, notes, achievements, and more!

**Now with organized folder structure!** 📁

![StudentFocus](https://img.shields.io/badge/StudentFocus-Ultimate%20Study%20Manager-6C63FF?style=for-the-badge)
![Firebase](https://img.shields.io/badge/Firebase-Realtime%20Database-FFCA28?style=for-the-badge)
![Single File](https://img.shields.io/badge/Single-HTML%20File-E34F26?style=for-the-badge)

---

## ✨ Features

### 📋 Task Management

- ✅ Add, edit, delete tasks
- ✅ Priority levels (High, Medium, Low)
- ✅ Categories (Homework, Project, Exam, Reading, Personal, Research, Presentation, Lab, Group)
- ✅ Due date tracking with overdue alerts
- ✅ Search and filter tasks
- ✅ Sort by date, priority, or creation time
- ✅ Export tasks to CSV
- ✅ Form validation with restrictions
- ✅ Stricter category limitations

### 🍅 Pomodoro Timer

- ✅ Customizable focus duration (1-60 mins)
- ✅ Short break (1-30 mins)
- ✅ Long break (1-60 mins)
- ✅ Auto-switch between focus and break
- ✅ Session tracking
- ✅ Ambient sound options (Rain, Forest, Café, Waves)
- ✅ Focus mode overlay

### 📊 Grade Tracker

- ✅ Add grades with scores (0-100)
- ✅ Credit-weighted GPA calculation
- ✅ Grade types (Exam, Quiz, Assignment, Project)
- ✅ Letter grade display (A-F)
- ✅ 4.0 scale GPA

### 📈 Study Analytics

- ✅ Daily study time tracking
- ✅ Weekly study chart
- ✅ Daily study goal with progress bar
- ✅ Study streak tracking

## 🎵 **Enhanced Features**

### 🎵 **Local Music Player**
- **5 Custom Tracks**: Pre-loaded focus music in `/music` folder
- **Track Navigation**: Next/Previous buttons for easy switching
- **Volume Control**: Adjustable slider with visual feedback
- **Personalization**: Replace with your own MP3 files (see [MUSIC_GUIDE.md](MUSIC_GUIDE.md))
- **Folder Created**: A `music/` folder has been created with placeholder files ready for your music

### 🖼️ **Picture-in-Picture Mode**
- **Floating Task Window**: Shows upcoming tasks in overlay
- **Mini Timer**: Compact Pomodoro timer that works over other apps
- **Real-time Updates**: Automatically refreshes with latest data

### ⚡ **Quick Task Creation**
- **Floating Button**: Always-accessible "+" button
- **Minimal Form**: Streamlined input for fast creation
- **Instant Submission**: Direct database integration

### 🔔 **Desktop Notifications**
- **Deadline Reminders**: 1-hour before due date alerts
- **System Integration**: Native browser notifications
- **Non-intrusive**: Auto-dismiss after 5 seconds
- ✅ Maximum daily study record

### 🏆 Achievements & Gamification

- ✅ 16+ unlockable achievements
- ✅ Study streak badges
- ✅ Task completion rewards
- ✅ Pomodoro milestones
- ✅ GPA achievements
- ✅ Early Bird & Night Owl badges

### 📝 Quick Notes

- ✅ Create colorful notes
- ✅ 5 color options
- ✅ Grid view layout
- ✅ Quick note taking

### 🎯 Focus Mode

- ✅ Distraction-free full-screen mode
- ✅ Motivational quotes
- ✅ Timer display
- ✅ Pause/Resume functionality

### 🌙 Theme & UX

- ✅ Dark/Light mode toggle
- ✅ Beautiful gradient UI
- ✅ Smooth animations
- ✅ Fully responsive design
- ✅ Keyboard shortcuts (Ctrl+N, Escape)
- ✅ Toast notifications

---

## 🚀 Quick Start

### 1️⃣ Firebase Setup

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project (or use existing)
3. Enable **Authentication** → **Email/Password**
4. Enable **Realtime Database**
5. Get your config from **Project Settings** → **Web App**

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    databaseURL: "https://YOUR_PROJECT-default-rtdb.firebaseio.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

1. Replace the config in `html/index.html` (search for `firebaseConfig`)

### 2️⃣ Database Rules

Go to **Realtime Database → Rules** and paste the rules from `firebase-database-rules.json`

---

## 🌐 Deployment Options

### 🐙 GitHub Pages

```bash
# 1. Create repository on GitHub
# 2. Push your code
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/studentfocus.git
git push -u origin main

# 3. Go to Settings → Pages → Select "main" branch → Save
# 4. Your app will be live at: https://YOUR_USERNAME.github.io/studentfocus
```

### ▲ Vercel

#### Option A: GitHub Integration (Recommended)

1. Go to [vercel.com](https://vercel.com)
2. Click **"Add New Project"**
3. Import your GitHub repository
4. Click **Deploy**
5. Done! 🎉

#### Option B: CLI

```bash
npm i -g vercel
vercel
vercel --prod
```

### 🔥 Firebase Hosting

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Initialize
firebase init
# Select: Hosting
# Public directory: . (or where index.html is)
# Single-page app: Yes
# Don't overwrite index.html

# Deploy
firebase deploy
```

### 📦 Netlify

1. Go to [netlify.com](https://netlify.com)
2. Drag and drop your folder
3. Done!

Or use CLI:

```bash
npm i -g netlify-cli
netlify deploy --prod
```

---

## 📁 Project Structure

```
studentfocus/
├── html/
│   └── index.html                # Main app (HTML structure)
├── css/
│   └── styles.css                # All CSS styles
├── js/
│   └── app.js                    # All JavaScript logic
├── assets/                       # Images, sounds, etc.
├── fire.json                     # Firebase database rules
└── README.md                     # Documentation
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + N` | Open new task form |
| `Escape` | Close modals/focus mode |

---

## 🎨 Customization

### Change Theme Colors

Find `:root` in CSS and modify:

```css
--primary: #6C63FF;     /* Main brand color */
--accent: #00d4aa;      /* Accent color */
--gradient: linear-gradient(135deg, #6C63FF 0%, #4ECDC4 100%);
```

### Add New Categories

1. Update the `<select>` options in `html/index.html`
2. Update the `allowedCategories` array in `js/app.js` validation
3. Update validation regex in database rules:

```javascript
"category": {
  ".validate": "newData.val().matches(/^(Homework|Project|Exam|Reading|Personal|Research|Presentation|Lab|Group)$/)"
}
```

### Add New Achievements

Add to the `achievementsList` array in `js/app.js`:

```javascript
{ 
  id: 'unique_id', 
  icon: '🎯', 
  title: 'Title', 
  desc: 'Description', 
  condition: (d) => d.someValue >= 10 
}
```

---

## 🔒 Security Features

- ✅ User data isolation (each user only sees their data)
- ✅ Input validation rules
- ✅ Length limits on all fields
- ✅ Enum validation for categories/priorities
- ✅ Number range validation for grades/settings
- ✅ Authenticated-only access

---

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| Mobile | ✅ Full |

---

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Database**: Firebase Realtime Database
- **Auth**: Firebase Authentication
- **Icons**: Font Awesome 6
- **Fonts**: Google Fonts (Poppins)

---

## 📊 Database Schema

```
├── users/{uid}
│   ├── name: string
│   ├── email: string
│   └── createdAt: number
│
├── tasks/{uid}/{taskId}
│   ├── title: string
│   ├── subject: string
│   ├── category: enum
│   ├── priority: enum
│   ├── dueDate: string
│   ├── completed: boolean
│   └── ...
│
├── grades/{uid}/{gradeId}
│   ├── subject: string
│   ├── score: number
│   ├── credits: number
│   └── type: enum
│
├── notes/{uid}/{noteId}
│   ├── title: string
│   ├── content: string
│   └── color: string
│
├── studyData/{uid}
│   ├── today: number
│   ├── weekly: array
│   ├── streak: number
│   └── ...
│
├── pomodoroStats/{uid}
│   ├── todayCount: number
│   ├── totalMinutes: number
│   └── lastSession: number
│
├── settings/{uid}
│   ├── focus: number
│   ├── shortBreak: number
│   ├── longBreak: number
│   └── dailyGoal: number
│
└── achievements/{uid}: array
```

---

## 🏆 Achievement List

### 🥇 Regular Achievements
| Icon | Name | Description |
|------|------|-------------|
| 🎯 | First Step | Add your first task |
| 📋 | Task Master | Complete 10 tasks |
| 🏆 | Task Legend | Complete 50 tasks |
| 🍅 | Pomodoro Starter | Complete 1 pomodoro |
| ⏰ | Focus Pro | Complete 25 pomodoros |
| 🔥 | On Fire | 3 day study streak |
| 💪 | Week Warrior | 7 day study streak |
| 🌟 | Monthly Master | 30 day study streak |
| 📚 | Honor Student | Get an A grade |
| 🎓 | Dean's List | Achieve 3.0+ GPA |
| 👑 | Perfect Scholar | Achieve 4.0 GPA |
| 🌅 | Early Bird | Study before 7 AM |
| 🦉 | Night Owl | Study after 11 PM |
| 📝 | Note Taker | Create 10 notes |
| 📖 | Dedicated | Study 2 hours in a day |
| 🧠 | Brain Power | Study 5 hours in a day |

### ⚡ Hard Mode Achievements
| Icon | Name | Description | Difficulty |
|------|------|-------------|------------|
| ⛩️ | Monk Mode | Study 12 hours in a day | Extreme |
| 🛡️ | Flawless Victory | 7 days of 100% task completion | Hard |
| 🚂 | Unstoppable | 365-day study streak | Legendary |

---

## 📄 License

MIT License - Feel free to use for personal or commercial projects!

---

## 🎯 Recent Enhancements

### 🎨 Customization
- Updated theme colors to `#6C63FF` (primary) and `#00d4aa` (accent)
- New gradient: `linear-gradient(135deg, #6C63FF 0%, #4ECDC4 100%)`

### 📋 New Categories
- Research (🔍)
- Presentation (📊)
- Lab (🧪)
- Group (👥)

### 🛡️ Enhanced Security
- Form validation with strict category restrictions
- Input length validation (title: 3+ chars, subject: 2+ chars)
- Estimated time validation (1-1440 minutes)
- Category dropdown validation

### 📁 Organized Structure
- Separate folders for HTML, CSS, and JavaScript
- Modular code organization
- Easier maintenance and customization

### 🚀 New Features Added

#### 🖼️ Picture-in-Picture Mode
- Floating task window that stays on top while browsing
- Mini Pomodoro timer that works over other applications
- Similar to YouTube's PiP feature in Brave browser
- Toggle between task and timer PiP modes

#### 🎵 Built-in Study Music Player
- Focus-enhancing background music
- Volume control with visual feedback
- Binaural beats for concentration
- Play/pause toggle with notification badge

#### ⚡ Quick Task Creation
- Floating "+" button for instant task entry
- Minimal form for rapid task creation
- Keyboard shortcut support
- Direct database integration

#### 🔔 Desktop Notifications
- System notifications for upcoming deadlines
- Automatic 1-hour before due date alerts
- Permission-based notification system
- Non-intrusive toast messages

#### 🎯 Enhanced User Experience
- Real-time updates across all components
- Smooth animations and transitions
- Mobile-responsive PiP modes
- Persistent user preferences

## 💖 Credits

Made with ❤️ for Students Worldwide 👉(SudhirDevOps1)

**StudentFocus © 2026**
