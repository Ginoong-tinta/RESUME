# RESUME

<?php
// Your personal information
$name = "MARK LLOYD L. TACDOL";
$course = "Bachelor of Science in Information Technology major in Database";
$jobTitle = "Associate Applications Leads";
$email = "john.doe@example.com";
$phone = "(123) 456-7890";
$address = "123 Main St, Cityville";

// Your skills
$skills = [
    "HTML",
    "CSS",
    "JavaScript",
    "PHP",
    "MySQL",
    "Responsive Design",
    "Git",
];

// Your education
$education = [
    ["B.S. in Computer Science", "University of Example", "2010 - 2014"],
];

// Your experience
$experience = [
    ["Web Developer", "ABC Company", "2015 - Present", "Developed and maintained web applications."],
    ["Intern, Software Engineering", "XYZ Tech", "2014 - 2015", "Assisted in software development projects."],
];

// Function to display skills
function displaySkills($skills) {
    echo "<ul>";
    foreach ($skills as $skill) {
        echo "<li>$skill</li>";
    }
    echo "</ul>";
}
?>

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><?php echo $name ?>'s Resume</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 40px;
        }

        h1,
        h2,
        h3 {
            margin-bottom: 5px;
        }

        .contact-info {
            margin-bottom: 20px;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin-bottom: 5px;
        }

        .section {
            margin-bottom: 20px;
        }
    </style>
</head>

<body>
    <header>
        <h1><?php echo $name ?></h1>
        <p><?php echo $course ?></p>
        <p><?php echo $jobTitle ?></p>
    </header>

    <div class="contact-info section">
        <h2>Contact Information</h2>
        <p>Email: <?php echo $email ?></p>
        <p>Phone: <?php echo $phone ?></p>
        <p>Address: <?php echo $address ?></p>
    </div>

    <div class="skills section">
        <h2>Skills</h2>
        <?php displaySkills($skills); ?>
    </div>

    <div class="education section">
        <h2>Education</h2>
        <ul>
            <?php
            foreach ($education as $edu) {
                echo "<li>$edu[0], $edu[1], $edu[2]</li>";
            }
            ?>
        </ul>
    </div>

    <div class="experience section">
        <h2>Experience</h2>
        <ul>
            <?php
            foreach ($experience as $exp) {
                echo "<li><strong>$exp[0]</strong>, $exp[1], $exp[2]<br>$exp[3]</li>";
            }
            ?>
        </ul>
    </div>
</body>

</html>
