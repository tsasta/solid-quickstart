<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Airline Departure Board Dashboard</title>
    <style>
        /* General body styling */
        body, html {
            font-family: 'Courier New', monospace;
            background-color: black; /* Setting the background to black */
            color: yellow; /* Changing text color to yellow */
            margin: 0;
            padding: 0;
        }

        /* Header styling */
        header h1 {
            background-color: #333; /* Darker background for the header */
            color: yellow; /* Maintaining yellow text for consistency */
            padding: 10px;
            text-align: center;
        }

        /* Table styling */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            border: 1px solid #555; /* Darker border for better visibility on a black background */
            text-align: center;
            padding: 8px;
        }

        /* Improving visibility and aesthetics */
        th {
            background-color: #555; /* Slightly lighter background for headers to stand out */
        }
    </style>
</head>
<body>
    <header>
        <h1>Airline Departure Information</h1>
    </header>
    <main>
        <table id="departureBoard">
            <!-- Dynamic rows will be inserted here by JavaScript -->
        </table>
    </main>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Here you would put your actual API fetching logic
            // For demonstration, we'll just create dummy data
            const data = [
                ['Flight', 'Destination', 'Time', 'Status'],
                ['AB123', 'New York', '08:00', 'On Time'],
                ['CD456', 'Los Angeles', '08:30', 'Delayed'],
                ['EF789', 'Chicago', '09:00', 'Cancelled'],
                ['GH012', 'Miami', '09:30', 'On Time'],
            ];

            const table = document.getElementById('departureBoard');
            data.forEach((row, index) => {
                let rowHTML = '<tr>';
                row.forEach(cell => {
                    rowHTML += `<td>${cell}</td>`;
                });
                rowHTML += '</tr>';
                table.innerHTML += rowHTML;
            });
        });
    </script>
</body>
</html>
