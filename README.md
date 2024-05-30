# Swagger-js-API

provides RESTful API endpoints for user authentication, managing blog posts, comments, and user interactions like liking and disliking posts and comments.

## Features

- User authentication (register/login)
- CRUD operations for blog posts
- CRUD operations for comments on blog posts
- Like and dislike functionality for posts and comments

## Getting Started

### Prerequisites

- Node.js
- npm/yarn

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/sanaz-shahraeini/Swagger-js-API.git
   ```
2. Install NPM packages:
   ```sh
   npm install
   ```
3. Run the application:
   ```sh
   npm run dev
   ```

### Using Swagger UI

The application includes Swagger UI for API documentation and interactive testing. After starting the application, visit `http://localhost:3000/api-docs` to access the Swagger UI interface.

## API Endpoints

| Endpoint                       | Method | Description             | Input                           | Output                    | Status Codes                      |
| ------------------------------ | ------ | ----------------------- | ------------------------------- | ------------------------- | --------------------------------- |
| `/auth/register`               | POST   | Register a new user     | `{ username, email, password }` | `{ id, username, email }` | 200 (OK), 400 (Bad Request)       |
| `/auth/login`                  | POST   | Log in a user           | `{ email, password }`           | `{ token }`               | 200 (OK), 401 (Unauthorized)      |
| `/users`                       | GET    | List all users          | N/A                             | `[users]`                 | 200 (OK)                          |
| `/posts`                       | GET    | List all posts          | N/A                             | `[posts]`                 | 200 (OK)                          |
| `/posts`                       | POST   | Create a new post       | `{ author, title, text }`       | `{ post }`                | 200 (OK), 400 (Bad Request)       |
| `/posts/{postId}`              | DELETE | Delete a post           | `{ postId }`                    | N/A                       | 204 (No Content), 404 (Not Found) |
| `/comments/{postId}`           | GET    | Get comments for a post | `{ postId }`                    | `[comments]`              | 200 (OK)                          |
| `/comments`                    | POST   | Create a comment        | `{ text, postId }`              | `{ comment }`             | 200 (OK), 400 (Bad Request)       |
| `/comments/delete/{commentId}` | DELETE | Delete a comment        | `{ commentId }`                 | N/A                       | 204 (No Content), 404 (Not Found) |

_Note: All POST and DELETE endpoints for posts and comments require authentication._

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your changes.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Ata Mohammadi - s.shahraeini@gmail.com


