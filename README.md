document.addEventListener('DOMContentLoaded', function() {
  // Delay the execution of the script by 5 seconds
  setTimeout(function() {
    // Fetch user data from sessionStorage
    const buyerData = sessionStorage.getItem('buyer');

    if (buyerData) {
      // Parse the buyer object
      const buyer = JSON.parse(buyerData);

      // Update the HTML elements with user details
      document.getElementById('userName').textContent = buyer.username; 
      document.getElementById('userEmail').textContent = "not available"; 
    } else {
      console.error('No buyer data found in sessionStorage.');
      // Optionally, redirect to the login page
      // window.location.href = "/login";
    }
  }, 5000); // 5000 milliseconds = 5 seconds
});
