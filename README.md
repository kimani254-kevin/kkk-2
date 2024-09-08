<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modal Example</title>
    <style>
        /* Basic styling for the button */
        .open-modal-btn {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 16px;
        }

        /* Style for the modal */
        .modal {
            display: none; 
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            justify-content: center;
            align-items: center;
        }

        /* Style for the modal content */
        .modal-content {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            width: 400px;
            text-align: left; /* Align text to the left */
        }

        /* Close button style */
        .close-btn {
            padding: 10px 15px;
            background-color: red;
            color: white;
            border: none;
            cursor: pointer;
            margin-top: 20px;
        }

        /* Centering the close button */
        .close-btn:hover {
            background-color: darkred;
        }
    </style>
</head>
<body>

<!-- Button to open the modal -->
<button class="open-modal-btn" onclick="openModal()">Enter Your Name</button>

<!-- Modal Structure -->
<div id="myModal" class="modal">
    <div class="modal-content">
        <h2>Enter Your Full Name</h2>
        <form>
            <label for="fullName">Full Name:</label>
            <input type="text" id="fullName" name="fullName">
            <br><br>
            <input type="submit" value="Submit">
        </form>
        <!-- Button to close the modal -->
        <button class="close-btn" onclick="closeModal()">Close</button>
    </div>
</div>

<script>
    // Function to open the modal
    function openModal() {
        document.getElementById('myModal').style.display = 'flex'; // Show the modal
    }

    // Function to close the modal
    function closeModal() {
        document.getElementById('myModal').style.display = 'none'; // Hide the modal
    }

    // Close the modal if the user clicks outside the modal content
    window.onclick = function(event) {
        const modal = document.getElementById('myModal');
        if (event.target == modal) {
            closeModal(); // Close the modal
        }
    }
</script>

</body>
</html>
