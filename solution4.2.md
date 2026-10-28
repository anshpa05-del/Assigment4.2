HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 4.2 — Job Application Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f9;
            margin: 20px;
            padding: 0;
        }
        form {
            max-width: 600px;
            background: #ffffff;
            padding: 25px;
            margin: 0 auto;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            font-weight: bold;
            margin-bottom: 5px;
            color: #444;
        }
        .inline-label {
            display: inline;
            font-weight: normal;
            margin-right: 15px;
        }
        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="url"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 14px;
        }
        input:disabled, select:disabled, textarea:disabled {
            background-color: #e9ecef;
            cursor: not-allowed;
        }
        .checkbox-group, .radio-group {
            margin-top: 5px;
        }
        button[type="submit"] {
            width: 100%;
            background-color: #28a745;
            color: white;
            border: none;
            padding: 12px;
            font-size: 16px;
            border-radius: 4px;
            cursor: pointer;
        }
        button[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <form action="#" method="POST">
        <h2>Job Application Form</h2>

        <!-- Disabled Field Example -->
        <div class="form-group">
            <label for="application-id">Application Reference ID (System Generated):</label>
            <input type="text" id="application-id" name="application_id" value="APP-2026-9876" disabled>
        </div>

        <!-- 1. Full name, email, and phone -->
        <div class="form-group">
            <label for="fullname">Full Name *</label>
            <input type="text" id="fullname" name="fullname" placeholder="John Doe" required>
        </div>

        <div class="form-group">
            <label for="email">Email Address *</label>
            <input type="email" id="email" name="email" placeholder="johndoe@example.com" required>
        </div>

        <div class="form-group">
            <label for="phone">Phone Number *</label>
            <input type="tel" id="phone" name="phone" placeholder="+1 123-456-7890" required>
        </div>

        <!-- 2. Date input for date of birth -->
        <div class="form-group">
            <label for="dob">Date of Birth *</label>
            <input type="date" id="dob" name="dob" required>
        </div>

        <!-- 3. URL input for portfolio URL -->
        <div class="form-group">
            <label for="portfolio">Portfolio URL</label>
            <input type="url" id="portfolio" name="portfolio" placeholder="https://myportfolio.com">
        </div>

        <!-- 4. Radio buttons for gender or preferred shift -->
        <div class="form-group">
            <label>Preferred Shift *</label>
            <div class="radio-group">
                <input type="radio" id="shift-day" name="preferred_shift" value="day" required>
                <label for="shift-day" class="inline-label">Day Shift</label>

                <input type="radio" id="shift-night" name="preferred_shift" value="night">
                <label for="shift-night" class="inline-label">Night Shift</label>

                <input type="radio" id="shift-flexible" name="preferred_shift" value="flexible">
                <label for="shift-flexible" class="inline-label">Flexible</label>
            </div>
        </div>

        <!-- 5. Checkboxes for skills -->
        <div class="form-group">
            <label>Technical Skills</label>
            <div class="checkbox-group">
                <input type="checkbox" id="skill-html" name="skills" value="HTML">
                <label for="skill-html" class="inline-label">HTML</label>

                <input type="checkbox" id="skill-css" name="skills" value="CSS">
                <label for="skill-css" class="inline-label">CSS</label>

                <input type="checkbox" id="skill-js" name="skills" value="JavaScript">
                <label for="skill-js" class="inline-label">JavaScript</label>

                <input type="checkbox" id="skill-react" name="skills" value="React">
                <label for="skill-react" class="inline-label">React</label>
            </div>
        </div>

        <!-- 6. Dropdown for qualification or job role -->
        <div class="form-group">
            <label for="job-role">Applied Job Role *</label>
            <select id="job-role" name="job_role" required>
                <option value="" disabled selected>Select a role...</option>
                <option value="frontend-developer">Frontend Developer</option>
                <option value="backend-developer">Backend Developer</option>
                <option value="fullstack-developer">Full Stack Developer</option>
                <option value="ui-ux-designer">UI/UX Designer</option>
            </select>
        </div>

        <!-- 7. <textarea> for cover letter -->
        <div class="form-group">
            <label for="cover-letter">Cover Letter *</label>
            <textarea id="cover-letter" name="cover_letter" rows="5" placeholder="Tell us why you're a great fit..." required></textarea>
        </div>

        <!-- 8. Submit button -->
        <button type="submit">Submit Application</button>
    </form>

</body>
</html>