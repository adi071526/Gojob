<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>GoJob - Hire Top Talent Worldwide</title>  
    <meta name="description" content="Hire skilled developers, designers, and professionals. Browse verified talent with ratings, degrees, and real experience.">  
    <style>  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
        }  
  
        body {  
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;  
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);  
            color: #e0e0e0;  
            min-height: 100vh;  
        }  
  
        .header {  
            background: rgba(26, 26, 46, 0.95);  
            backdrop-filter: blur(10px);  
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);  
            padding: 1.5rem 2rem;  
            position: sticky;  
            top: 0;  
            z-index: 100;  
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);  
        }  
  
        .header-content {  
            max-width: 1400px;  
            margin: 0 auto;  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
        }  
  
        .logo-section {  
            display: flex;  
            align-items: center;  
            gap: 1rem;  
        }  
  
        .logo {  
            width: 50px;  
            height: 50px;  
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            border-radius: 12px;  
            display: flex;  
            align-items: center;  
            justify-content: center;  
            font-size: 1.5rem;  
            font-weight: 700;  
            color: white;  
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.4);  
        }  
  
        .logo-text h1 {  
            font-size: 2rem;  
            background: linear-gradient(135deg, #a78bfa, #c4b5fd);  
            -webkit-background-clip: text;  
            -webkit-text-fill-color: transparent;  
            background-clip: text;  
        }  
  
        .logo-text p {  
            font-size: 0.85rem;  
            color: #9ca3af;  
        }  
  
        .header-buttons {  
            display: flex;  
            gap: 1rem;  
        }  
  
        .btn {  
            padding: 0.75rem 1.5rem;  
            border-radius: 10px;  
            font-weight: 600;  
            cursor: pointer;  
            transition: all 0.3s ease;  
            border: none;  
            font-size: 1rem;  
        }  
  
        .btn-primary {  
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            color: white;  
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);  
        }  
  
        .btn-primary:hover {  
            transform: translateY(-2px);  
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.5);  
        }  
  
        .btn-secondary {  
            background: rgba(102, 126, 234, 0.1);  
            color: #a78bfa;  
            border: 1px solid rgba(102, 126, 234, 0.3);  
        }  
  
        .btn-secondary:hover {  
            background: rgba(102, 126, 234, 0.2);  
        }  
  
        .container {  
            max-width: 1400px;  
            margin: 0 auto;  
            padding: 2rem;  
        }  
  
        .hero {  
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);  
            border: 1px solid rgba(102, 126, 234, 0.2);  
            border-radius: 24px;  
            padding: 3rem;  
            margin-bottom: 2rem;  
            backdrop-filter: blur(10px);  
        }  
  
        .hero h2 {  
            font-size: 3rem;  
            margin-bottom: 1rem;  
            background: linear-gradient(135deg, #a78bfa, #c4b5fd);  
            -webkit-background-clip: text;  
            -webkit-text-fill-color: transparent;  
            background-clip: text;  
        }  
  
        .hero p {  
            font-size: 1.2rem;  
            color: #9ca3af;  
            margin-bottom: 2rem;  
        }  
  
        .search-box {  
            position: relative;  
            margin-bottom: 2rem;  
        }  
  
        .search-box input {  
            width: 100%;  
            padding: 1.25rem 1.25rem 1.25rem 3.5rem;  
            background: rgba(26, 26, 46, 0.8);  
            border: 1px solid rgba(255, 255, 255, 0.2);  
            border-radius: 16px;  
            color: #e0e0e0;  
            font-size: 1.1rem;  
            transition: all 0.3s ease;  
        }  
  
        .search-box input:focus {  
            outline: none;  
            border-color: #667eea;  
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);  
        }  
  
        .search-icon {  
            position: absolute;  
            left: 1.25rem;  
            top: 50%;  
            transform: translateY(-50%);  
            color: #9ca3af;  
        }  
  
        .categories {  
            display: flex;  
            gap: 1rem;  
            margin-bottom: 2rem;  
            overflow-x: auto;  
            padding-bottom: 0.5rem;  
        }  
  
        .category-btn {  
            padding: 0.75rem 1.5rem;  
            background: rgba(42, 42, 62, 0.6);  
            border: 1px solid rgba(255, 255, 255, 0.1);  
            border-radius: 12px;  
            color: #e0e0e0;  
            cursor: pointer;  
            transition: all 0.3s ease;  
            white-space: nowrap;  
            font-size: 1rem;  
        }  
  
        .category-btn:hover, .category-btn.active {  
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            border-color: transparent;  
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);  
        }  
  
        .stats {  
            display: grid;  
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));  
            gap: 1.5rem;  
            margin-bottom: 2rem;  
        }  
  
        .stat-card {  
            background: rgba(42, 42, 62, 0.6);  
            border: 1px solid rgba(255, 255, 255, 0.1);  
            border-radius: 16px;  
            padding: 1.5rem;  
            backdrop-filter: blur(10px);  
        }  
  
        .stat-card h3 {  
            font-size: 2.5rem;  
            margin-bottom: 0.5rem;  
            color: #a78bfa;  
        }  
  
        .stat-card p {  
            color: #9ca3af;  
        }  
  
        .employees-grid {  
            display: grid;  
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));  
            gap: 2rem;  
            margin-bottom: 2rem;  
        }  
  
        .employee-card {  
            background: rgba(42, 42, 62, 0.6);  
            border: 1px solid rgba(255, 255, 255, 0.1);  
            border-radius: 20px;  
            padding: 1.5rem;  
            transition: all 0.3s ease;  
            cursor: pointer;  
            backdrop-filter: blur(10px);  
            position: relative;  
        }  
  
        .employee-card:hover {  
            transform: translateY(-5px);  
            border-color: #667eea;  
            box-shadow: 0 12px 24px rgba(102, 126, 234, 0.3);  
        }  
  
        .employee-header {  
            display: flex;  
            gap: 1rem;  
            margin-bottom: 1rem;  
        }  
  
        .employee-avatar {  
            font-size: 4rem;  
        }  
  
        .employee-info h3 {  
            font-size: 1.3rem;  
            margin-bottom: 0.25rem;  
            color: white;  
        }  
  
        .employee-info p {  
            font-size: 0.9rem;  
            color: #9ca3af;  
        }  
  
        .employee-meta {  
            display: flex;  
            gap: 1rem;  
            margin-bottom: 1rem;  
            font-size: 0.9rem;  
        }  
  
        .rating {  
            color: #fbbf24;  
        }  
  
        .location {  
            color: #9ca3af;  
        }  
  
        .education {  
            background: rgba(102, 126, 234, 0.1);  
            padding: 0.75rem;  
            border-radius: 10px;  
            margin-bottom: 1rem;  
        }  
  
        .education p {  
            font-size: 0.9rem;  
        }  
  
        .education p:first-child {  
            font-weight: 600;  
            color: #a78bfa;  
            margin-bottom: 0.25rem;  
        }  
  
        .skills {  
            display: flex;  
            flex-wrap: wrap;  
            gap: 0.5rem;  
            margin-bottom: 1rem;  
        }  
  
        .skill-tag {  
            padding: 0.5rem 1rem;  
            background: rgba(102, 126, 234, 0.2);  
            border: 1px solid rgba(102, 126, 234, 0.3);  
            border-radius: 20px;  
            font-size: 0.85rem;  
            color: #c4b5fd;  
        }  
  
        .employee-footer {  
            display: flex;  
            justify-content: space-between;  
            align-items: center;  
            padding-top: 1rem;  
            border-top: 1px solid rgba(255, 255, 255, 0.1);  
        }  
  
        .employee-stats {  
            display: flex;  
            gap: 1rem;  
            font-size: 0.85rem;  
            color: #9ca3af;  
        }  
  
        .hourly-rate {  
            font-size: 1.5rem;  
            font-weight: 700;  
            color: #10b981;  
        }  
  
        .modal {  
            display: none;  
            position: fixed;  
            top: 0;  
            left: 0;  
            width: 100%;  
            height: 100%;  
            background: rgba(0, 0, 0, 0.8);  
            backdrop-filter: blur(5px);  
            z-index: 1000;  
            justify-content: center;  
            align-items: center;  
            padding: 2rem;  
        }  
  
        .modal.active {  
            display: flex;  
        }  
  
        .modal-content {  
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);  
            border: 1px solid rgba(255, 255, 255, 0.2);  
            border-radius: 24px;  
            max-width: 600px;  
            width: 100%;  
            max-height: 90vh;  
            overflow-y: auto;  
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);  
        }  
  
        .modal-header {  
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);  
            padding: 2rem;  
            border-radius: 24px 24px 0 0;  
            position: relative;  
        }  
  
        .modal-header h2 {  
            color: white;  
            font-size: 2rem;  
            margin-bottom: 0.5rem;  
        }  
  
        .close-btn {  
            position: absolute;  
            top: 1rem;  
            right: 1rem;  
            background: rgba(255, 255, 255, 0.2);  
            border: none;  
            width: 40px;  
            height: 40px;  
            border-radius: 50%;  
            font-size: 1.5rem;  
            color: white;  
            cursor: pointer;  
            transition: all 0.3s ease;  
        }  
  
        .close-btn:hover {  
            background: rgba(255, 255, 255, 0.3);  
        }  
  
        .modal-body {  
            padding: 2rem;  
        }  
  
        .form-group {  
            margin-bottom: 1.5rem;  
        }  
  
        .form-group label {  
            display: block;  
            margin-bottom: 0.5rem;  
            color: #a78bfa;  
            font-weight: 600;  
        }  
  
        .form-group input,  
        .form-group select,  
        .form-group textarea {  
            width: 100%;  
            padding: 0.75rem;  
            background: rgba(26, 26, 46, 0.8);  
            border: 1px solid rgba(255, 255, 255, 0.2);  
            border-radius: 10px;  
            color: #e0e0e0;  
            font-size: 1rem;  
            font-family: inherit;  
        }  
  
        .form-group input:focus,  
        .form-group select:focus,  
        .form-group textarea:focus {  
            outline: none;  
            border-color: #667eea;  
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);  
        }  
  
        .avatar-selector {  
            display: flex;  
            flex-wrap: wrap;  
            gap: 0.5rem;  
        }  
  
        .avatar-option {  
            font-size: 2rem;  
            padding: 0.5rem;  
            cursor: pointer;  
            border: 2px solid transparent;  
            border-radius: 10px;  
            transition: all 0.3s ease;  
        }  
  
        .avatar-option:hover,  
        .avatar-option.selected {  
            border-color: #667eea;  
            background: rgba(102, 126, 234, 0.2);  
        }  
  
        .form-actions {  
            display: flex;  
            gap: 1rem;  
            margin-top: 2rem;  
        }  
  
        .no-results {  
            text-align: center;  
            padding: 4rem 2rem;  
        }  
  
        .no-results-icon {  
            font-size: 5rem;  
            margin-bottom: 1rem;  
        }  
  
        .no-results h3 {  
            color: #9ca3af;  
            font-size: 1.5rem;  
        }  
  
        @media (max-width: 768px) {  
            .hero h2 {  
                font-size: 2rem;  
            }  
  
            .employees-grid {  
                grid-template-columns: 1fr;  
            }  
  
            .header-content {  
                flex-direction: column;  
                gap: 1rem;  
            }  
        }  
    </style>  
</head>  
<body>  
    <header class="header">  
        <div class="header-content">  
            <div class="logo-section">  
                <div class="logo">GJ</div>  
                <div class="logo-text">  
                    <h1>GoJob</h1>  
                    <p>Find Your Perfect Talent</p>  
                </div>  
            </div>  
            <div class="header-buttons">  
                <button class="btn btn-secondary" onclick="openAddModal()">+ Add Talent</button>  
                <button class="btn btn-primary">Sign In</button>  
            </div>  
        </div>  
    </header>  
  
    <div class="container">  
        <div class="hero">  
            <h2>Hire Top Talent Today</h2>  
            <p>Connect with skilled professionals worldwide</p>  
            <div class="search-box">  
                <svg class="search-icon" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">  
                    <circle cx="11" cy="11" r="8"></circle>  
                    <path d="m21 21-4.35-4.35"></path>  
                </svg>  
                <input type="text" id="searchInput" placeholder="Search by name, skills, or job title..." oninput="filterEmployees()">  
            </div>  
        </div>  
  
        <div class="categories">  
            <button class="category-btn active" onclick="filterCategory('all')">All Categories</button>  
            <button class="category-btn" onclick="filterCategory('development')">Development</button>  
            <button class="category-btn" onclick="filterCategory('design')">Design</button>  
            <button class="category-btn" onclick="filterCategory('marketing')">Marketing</button>  
            <button class="category-btn" onclick="filterCategory('business')">Business</button>  
        </div>  
  
        <div class="stats">  
            <div class="stat-card">  
                <h3 id="totalTalents">0</h3>  
                <p>Available Talents</p>  
            </div>  
            <div class="stat-card">  
                <h3 id="avgRating">0</h3>  
                <p>Average Rating</p>  
            </div>  
            <div class="stat-card">  
                <h3 id="totalJobs">0</h3>  
                <p>Jobs Completed</p>  
            </div>  
            <div class="stat-card">  
                <h3 id="successRate">0%</h3>  
                <p>Success Rate</p>  
            </div>  
        </div>  
  
        <div class="employees-grid" id="employeesGrid"></div>  
    </div>  
  
    <!-- Add Employee Modal -->  
    <div class="modal" id="addModal">  
        <div class="modal-content">  
            <div class="modal-header">  
                <h2>Add New Talent</h2>  
                <button class="close-btn" onclick="closeAddModal()">×</button>  
            </div>  
            <div class="modal-body">  
                <form id="addEmployeeForm" onsubmit="addEmployee(event)">  
                    <div class="form-group">  
                        <label>Full Name *</label>  
                        <input type="text" name="name" required placeholder="John Doe">  
                    </div>  
                    <div class="form-group">  
                        <label>Job Title *</label>  
                        <input type="text" name="title" required placeholder="Full Stack Developer">  
                    </div>  
                    <div class="form-group">  
                        <label>Avatar</label>  
                        <div class="avatar-selector">  
                            <span class="avatar-option selected" onclick="selectAvatar(this)">👨‍💻</span>  
                            <span class="avatar-option" onclick="selectAvatar(this)">👩‍💻</span>  
                            <span class="avatar-option" onclick="selectAvatar(this)">👨‍🎨</span>  
                            <span class="avatar-option" onclick="selectAvatar(this)">👩‍🎨</span>  
                            <span class="avatar-option" onclick="selectAvatar(this)">👨‍💼</span>  
                            <span class="avatar-option" onclick="selectAvatar(this)">👩‍💼</span>  
                        </div>  
                        <input type="hidden" name="avatar" value="👨‍💻">  
                    </div>  
                    <div class="form-group">  
                        <label>Category *</label>  
                        <select name="category" required>  
                            <option value="development">Development</option>  
                            <option value="design">Design</option>  
                            <option value="marketing">Marketing</option>  
                            <option value="business">Business</option>  
                        </select>  
                    </div>  
                    <div class="form-group">  
                        <label>Hourly Rate ($) *</label>  
                        <input type="number" name="hourlyRate" required min="1" value="50">  
                    </div>  
                    <div class="form-group">  
                        <label>Location *</label>  
                        <input type="text" name="location" required placeholder="New York, NY">  
                    </div>  
                    <div class="form-group">  
                        <label>Experience *</label>  
                        <input type="text" name="experience" required placeholder="5 years">  
                    </div>  
                    <div class="form-group">  
                        <label>Skills (comma-separated) *</label>  
                        <input type="text" name="skills" required placeholder="React, Node.js, TypeScript">  
                    </div>  
                    <div class="form-group">  
                        <label>Degree *</label>  
                        <input type="text" name="degree" required placeholder="BS Computer Science">  
                    </div>  
                    <div class="form-group">  
                        <label>University *</label>  
                        <input type="text" name="university" required placeholder="MIT">  
                    </div>  
                    <div class="form-group">  
                        <label>Bio *</label>  
                        <textarea name="bio" required rows="3" placeholder="Brief description about the talent..."></textarea>  
                    </div>  
                    <div class="form-actions">  
                        <button type="submit" class="btn btn-primary" style="flex: 1;">Add Talent</button>  
                        <button type="button" class="btn btn-secondary" style="flex: 1;" onclick="closeAddModal()">Cancel</button>  
                    </div>  
                </form>  
            </div>  
        </div>  
    </div>  
  
    <script>  
        let employees = [];  
        let currentCategory = 'all';  
  
        // Initialize  
        window.onload = function() {  
            loadEmployees();  
        };  
  
        function loadEmployees() {  
            const stored = localStorage.getItem('gojob_employees');  
            if (stored) {  
                employees = JSON.parse(stored);  
            } else {  
                // Load sample data  
                employees = [  
                    {  
                        id: Date.now() + 1,  
                        name: 'Sarah Chen',  
                        title: 'Senior Full Stack Developer',  
                        avatar: '👩‍💻',  
                        rating: 4.9,  
                        reviews: 127,  
                        hourlyRate: 85,  
                        location: 'San Francisco, CA',  
                        skills: ['React', 'Node.js', 'TypeScript', 'AWS'],  
                        degree: 'MS Computer Science',  
                        university: 'Stanford University',  
                        experience: '8 years',  
                        category: 'development',  
                        completedJobs: 156,  
                        successRate: 98,  
                        bio: 'Specialized in building scalable web applications.'  
                    },  
                    {  
                        id: Date.now() + 2,  
                        name: 'Marcus Johnson',  
                        title: 'UI/UX Designer',  
                        avatar: '👨‍🎨',  
                        rating: 5.0,  
                        reviews: 89,  
                        hourlyRate: 75,  
                        location: 'New York, NY',  
                        skills: ['Figma', 'Adobe XD', 'Prototyping'],  
                        degree: 'BFA Design',  
                        university: 'Parsons',  
                        experience: '6 years',  
                        category: 'design',  
                        completedJobs: 134,  
                        successRate: 100,  
                        bio: 'Award-winning designer creating intuitive experiences.'  
                    }  
                ];  
                saveEmployees();  
            }  
            renderEmployees();  
            updateStats();  
        }  
  
        function saveEmployees() {  
            localStorage.setItem('gojob_employees', JSON.stringify(employees));  
        }  
  
        function renderEmployees() {  
            const grid = document.getElementById('employeesGrid');  
            const searchQuery = document.getElementById('searchInput').value.toLowerCase();  
              
            const filtered = employees.filter(emp => {  
                const matchesCategory = currentCategory === 'all' || emp.category === currentCategory;  
                const matchesSearch = emp.name.toLowerCase().includes(searchQuery) ||  
                                     emp.title.toLowerCase().includes(searchQuery) ||  
                                     emp.skills.some(s => s.toLowerCase().includes(searchQuery));  
                return matchesCategory && matchesSearch;  
            });  
  
            if (filtered.length === 0) {  
                grid.innerHTML = `  
                    <div class="no-results" style="grid-column: 1/-1;">  
                        <div class="no-results-icon">🔍</div>  
                        <h3>No talents found</h3>  
                        <p>Try adjusting your search or filters</p>  
                    </div>  
                `;  
                return;  
            }  
  
            grid.innerHTML = filtered.map(emp => `  
                <div class="employee-card">  
                    <div class="employee-header">  
                        <div class="employee-avatar">${emp.avatar}</div>  
                        <div class="employee-info">  
                            <h3>${emp.name}</h3>  
                            <p>${emp.title}</p>  
                        </div>  
                    </div>  
                    <div class="employee-meta">  
                        <span class="rating">⭐ ${emp.rating} (${emp.reviews})</span>  
                        <span class="location">📍 ${emp.location}</span>  
                    </div>  
                    <div class="education">  
                        <p>${emp.degree}</p>  
                        <p style="color: #9ca3af; font-size: 0.85rem;">${emp.university}</p>  
                    </div>  
                    <div class="skills">  
                        ${emp.skills.slice(0, 4).map(skill => `<span class="skill-tag">${skill}</span>`).join('')}  
                        ${emp.skills.length > 4 ? `<span class="skill-tag">+${emp.skills.length - 4}</span>` : ''}  
                    </div>  
                    <div class="employee-footer">  
                        <div class="employee-stats">  
                            <span>💼 ${emp.completedJobs} jobs</span>  
                            <span>📈 ${emp.successRate}%</span>  
                        </div>  
                        <div class="hourly-rate">$${emp.hourlyRate}/hr</div>  
                    </div>  
                </div>  
            `).join('');  
        }  
  
        function updateStats() {  
            document.getElementById('totalTalents').textContent = employees.length;  
              
            if (employees.length > 0) {  
                const avgRating = (employees.reduce((sum, e) => sum + e.rating, 0) / employees.length).toFixed(1);  
                const totalJobs = employees.reduce((sum, e) => sum + e.completedJobs, 0);  
                const avgSuccess = Math.round(employees.reduce((sum, e) => sum + e.successRate, 0) / employees.length);  
                  
                document.getElementById('avgRating').textContent = avgRating;  
                document.getElementById('totalJobs').textContent = totalJobs;  
                document.getElementById('successRate').textContent = avgSuccess + '%';  
            }  
        }  
  
        function filterCategory(category) {  
            currentCategory = category;  
            document.querySelectorAll('.category-btn').forEach(btn => btn.classList.remove('active'));  
            event.target.classList.add('active');  
            renderEmployees();  
        }  
  
        function filterEmployees() {  
            renderEmployees();  
        }  
  
        function openAddModal() {  
            document.getElementById('addModal').classList.add('active');  
        }  
  
        function closeAddModal() {  
            document.getElementById('addModal').classList.remove('active');  
            document.getElementById('addEmployeeForm').reset();  
        }  
  
        function selectAvatar(element) {  
            document.querySelectorAll('.avatar-option').forEach(opt => opt.classList.remove('selected'));  
            element.classList.add('selected');  
            document.querySelector('input[name="avatar"]').value = element.textContent;  
        }  
  
        function addEmployee(event) {  
            event.preventDefault();  
            const formData = new FormData(event.target);  
              
            const newEmployee = {  
                id: Date.now(),  
                name: formData.get('name'),  
                title: formData.get('title'),  
                avatar: formData.get('avatar'),  
                rating: 5.0,  
                reviews: 0,  
                hourlyRate: parseInt(formData.get('hourlyRate')),  
                location: formData.get('location'),  
                skills: formData.get('skills').split(',').map(s => s.trim()),  
                degree: formData.get('degree'),  
                university: formData.get('university'),  
                experience: formData.get('experience'),  
                category: formData.get('category'),  
                completedJobs: 0,  
                successRate: 100,  
                bio: formData.get('bio')  
            };  
  
            employees.push(newEmployee);  
            saveEmployees();  
            renderEmployees();  
            updateStats();  
            closeAddModal();  
              
            alert('✅ Talent added successfully!');  
        }  
    </script>  
</body>  
</html>  
