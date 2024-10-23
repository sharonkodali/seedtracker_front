---
layout: post
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
    <title>Student Table</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        table, th, td {
            border: 1px solid black;
            padding: 10px;
            text-align: left;
        }
    </style>
</head>
<body>

<h2>Student List</h2>

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
