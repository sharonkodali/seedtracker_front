---
layout: base
title: Seed Tracker
categories: [Collaboration]
courses: { csse: {week: 3}, csp: {week: 3}, csa: {week: 2} }
permalink: /seedy
type: collab
comments: true
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Super Seed Tracker</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
        }

        h2 {
            text-align: center;
            margin-top: 20px;
            font-weight: 500;
        }

        .table-container {
            width: 80%;
            margin: 20px auto;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        th, td {
            padding: 15px;
            text-align: left;
        }

        th {
            background-color: #4CAF50;
            color: white;
            font-size: 16px;
            font-weight: 500;
        }

        td {
            background-color: #000; /* Black color for odd rows */
            color: #fff;
        }

        tr:nth-child(even) td {
            background-color: #0a1172; /* Dark blue for even rows */
        }

        tr:hover td {
            background-color: #4CAF50; /* Hover effect */
            color: #000; /* Change text to black on hover */
        }

        input[type="text"] {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 14px;
            outline: none;
            transition: border-color 0.3s ease;
        }

        input[type="text"]:focus {
            border-color: #4CAF50;
        }

        .table-footer {
            text-align: right;
            padding: 15px;
            background-color: #f9f9f9;
            font-weight: 500;
            color: #555;
        }
    </style>
</head>
<body>

<h2>Student List</h2>

<div class="table-container">
    <table id="studentTable">
        <tr>
            <th>Name</th>
            <th>Seed</th>
            <th>Comments</th>
        </tr>
        <tr>
            <td>Example Student</td>
            <td></td>
            <td><input type="text" placeholder="Add comment"></td>
        </tr>
    </table>
</div>

<script>
    function addRows() {
        const table = document.getElementById("studentTable");
        for (let i = 1; i < 26; i++) {
            const row = table.insertRow();
            const nameCell = row.insertCell(0);
            const seedCell = row.insertCell(1);
            const commentCell = row.insertCell(2);

            nameCell.textContent = "Example Student";
            seedCell.textContent = ""; // Leave it empty for now
            const commentInput = document.createElement("input");
            commentInput.type = "text";
            commentInput.placeholder = "Add comment";
            commentCell.appendChild(commentInput);
        }
    }

    // Automatically add the rows when the page loads
    window.onload = addRows;
</script>

</body>
</html>
