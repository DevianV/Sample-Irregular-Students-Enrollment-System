# Quick Start - Testing the System

## 🚀 3-Step Setup

### Step 1: Setup Database (2 minutes)

**Option A: Using Command Line**
```bash
mysql -u root -p < db/init.sql
```

**Option B: Using phpMyAdmin**
1. Open http://localhost/phpmyadmin
2. Click "New" → Database name: `plm_enrollment_db`
3. Click "Import" → Select `db/init.sql` → Click "Go"

### Step 2: Start Web Server (30 seconds)

Open terminal/command prompt in project folder and run:
```bash
php -S localhost:8000
```

You should see:
```
PHP 7.x.x Development Server started at http://localhost:8000
```

### Step 3: Open Browser (10 seconds)

Go to: **http://localhost:8000**

---

## ✅ Quick Verification

Run this command to verify everything is set up:
```bash
php quick_test.php
```

You should see all ✅ checkmarks!

---

## 🔑 Test Login Credentials

**Irregular Student (Can Login):**
- Student ID: `2020-12345`
- Password: `password123`
- Name: Juan Dela Cruz
- Already passed: CS101, CS102

**Regular Student (Will be Denied):**
- Student ID: `2020-12347`
- Password: `password123`
- Expected: "Access denied" message

---

## 🧪 Basic Test Flow

1. **Login** → Use `2020-12345` / `password123`
2. **Dashboard** → Check Personal Info, Grades, Taken Subjects tabs
3. **Enroll** → Click "Enroll" button
4. **Add Subjects** → Try adding CS201 or CS202
5. **Finalize** → Click "Finalize Enrollment"
6. **SER** → Click "Print SER" button

---

## ⚠️ Common Issues

**"Database connection failed"**
- Check MySQL is running
- Update `config.php` with your MySQL password

**"Invalid password"**
- Password is: `password123` (all lowercase, no spaces)
- If still fails, run: `php generate_password.php` to generate new hash

**"No subjects showing"**
- Check `CURRENT_SEMESTER` in `config.php` matches database
- Verify student's program matches subjects

---

## 📚 More Details

- See `TESTING.md` for comprehensive test scenarios
- See `SETUP.md` for detailed installation guide

---

**That's it! You're ready to test! 🎉**

