const axios = require('axios');

// Function to create a repository
async function createRepository(repoName, token) {
  try {
    // Send a POST request to the GitHub API to create a new repository
    const response = await axios.post('https://api.github.com/user/repos', {
      name: repoName,
      private: false
    }, {
      headers: {
        'Authorization': token ${token},
        'Accept': 'application/vnd.github.v3+json'
      }
    });

    // Output the success message if the repository is created successfully
    console.log(Repository "${response.data.name}" created successfully!);
  } catch (error) {
    // Output the error message if there's an error creating the repository
    console.error('Error creating repository:', error.message);
  }
}

// Replace 'YOUR_ACCESS_TOKEN' with your own GitHub access token
const accessToken = 'YOUR_ACCESS_TOKEN';
const repositoryName = 'my-new-repo';

// Call the createRepository function with the repository name and access token
createRepository(repositoryName, accessToken);
// Replace 'YOUR_ACCESS_TOKEN' with your own GitHub access token
const accessToken = 'YOUR_ACCESS_TOKEN';
const repositoryName = 'my-new-repo';

// Call the createRepository function with the repository name and access token
createRepository(repositoryName, accessToken);
