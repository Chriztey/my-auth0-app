<div align="center">
  <h1>🔐 Auth0 Authentication System</h1>
  <p><i>A "Server-First" secure authentication starter for Next.js 15 projects.</i></p>
</div>

<hr />

<h2>🚀 Quick Start Guide</h2>
<p>Follow these steps to get the demo running on your local machine.</p>

<details open>
  <summary><b>1. Clone the Repository</b></summary>
  <p>Open your terminal and run the following commands:</p>
  <pre><code>git clone https://github.com/Chriztey/my-auth0-app
cd my-auth0-app</code></pre>
</details>

<details open>
  <summary><b>2. Configure Environment Variables</b></summary>
  <p>Auth0 uses environment variables to secure your application. Create a <code>.env.local</code> file in the root directory and add the following:</p>
  <pre><code>AUTH0_DOMAIN={yourDomain}.auth0.com
AUTH0_CLIENT_ID={yourClientId}
AUTH0_CLIENT_SECRET={yourClientSecret}
AUTH0_SECRET={generated_32_char_secret}
APP_BASE_URL=http://localhost:3000</code></pre>
  <p><i>Tip: Run <code>openssl rand -hex 32</code> in your terminal to generate a secure AUTH0_SECRET.</i></p>
</details>

<details open>
  <summary><b>3. Install & Run</b></summary>
  <p>Install the dependencies and start the development server:</p>
  <pre><code>npm install
npm run dev</code></pre>
</details>

<blockquote style="background-color: #fff5f5; border-left: 5px solid #ff5a5f; padding: 10px;">
  <strong>⚠️ Note:</strong> Ensure your Auth0 Dashboard has <code>http://localhost:3000/auth/callback</code> in <b>Allowed Callback URLs</b> and <code>http://localhost:3000</code> in <b>Allowed Logout URLs</b>.
</blockquote>

<hr />

<h2>🏗️ Architecture Overview</h2>

<p align="center">
  
</p>

<p>This app utilizes the <b>Auth0 Next.js SDK v4</b>, moving authentication logic to the <b>Server-Side</b>. This eliminates client-side "flashes" and provides a more secure session management system.</p>

<ul>
  <li><b><code>src/lib/auth0.ts</code></b>: Initializes the <code>Auth0Client</code> for server-side session handling.</li>
  <li><b><code>src/middleware.ts</code></b>: The "Edge Gatekeeper." It handles authentication routes (<code>/auth/*</code>) and protects private pages before they render.</li>
  <li><b><code>Auth0Provider</code></b>: Wrapped in the root layout to provide user context to client-side components.</li>
</ul>

<hr />

<h2>🔑 The Entry Gate</h2>
<p>For this demo, two primary login methods are enabled via the <b>Auth0 Universal Login</b> page:</p>
<ul>
  <li><b>Email & Password:</b> Standard registration flow (requires signing up first).</li>
  <li><b>Google OAuth:</b> Instant social login for rapid testing.</li>
</ul>

<hr />

<div align="center">
  <p><a href="https://github.com/Chriztey">Chriztey</a></p>
</div>
