<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AMEX Airline Partnership Ecosystem</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/lucide-static@0.263.0/font/lucide.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .tab-active {
            border-bottom: 2px solid #2563eb;
            color: #2563eb;
        }
        .metric-card {
            transition: all 0.3s ease;
        }
        .metric-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }
        .airline-item {
            transition: all 0.3s ease;
        }
        .airline-item:hover {
            transform: translateY(-1px);
        }
        .flow-step {
            position: relative;
        }
        .flow-step:not(:last-child)::after {
            content: '';
            position: absolute;
            left: 1rem;
            bottom: -1.5rem;
            width: 2px;
            height: 1.5rem;
            background-color: #93c5fd;
        }
        .lounge-tier {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        .merchant-tier {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
        }
        .gradient-header {
            background: linear-gradient(135deg, #1e3a8a 0%, #3b82f6 100%);
        }
        .card-hover {
            transition: all 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-slate-50 to-blue-50 min-h-screen">
    <!-- Header -->
    <header class="gradient-header text-white shadow-lg">
        <div class="container mx-auto px-4 py-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center space-x-4 mb-4 md:mb-0">
                    <div class="bg-white p-3 rounded-xl shadow-lg">
                        <i class="fas fa-credit-card text-blue-600 text-2xl"></i>
                    </div>
                    <div>
                        <h1 class="text-3xl font-bold">AMEX Airline Partnership Ecosystem</h1>
                        <p class="text-blue-100">Cash flows, relationships, and party responsibilities</p>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <div class="bg-blue-500 bg-opacity-30 rounded-lg p-2 flex items-center">
                        <i class="fas fa-calendar-alt mr-2"></i>
                        <select id="timeframe-selector" class="bg-transparent text-white font-medium focus:outline-none">
                            <option value="annual">Annual View</option>
                            <option value="quarterly">Quarterly View</option>
                        </select>
                    </div>
                    <div class="hidden md:flex items-center space-x-2 text-sm">
                        <div class="w-3 h-3 bg-green-500 rounded-full"></div>
                        <span>Live Data</span>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="bg-white shadow-sm sticky top-0 z-10">
        <div class="container mx-auto px-4">
            <div class="flex overflow-x-auto py-2 space-x-1">
                <button data-tab="relationships" class="tab-button px-4 py-3 font-medium transition-colors tab-active whitespace-nowrap">
                    <i class="fas fa-handshake mr-2"></i>Partner Relationships
                </button>
                <button data-tab="lounges" class="tab-button px-4 py-3 font-medium transition-colors text-gray-600 hover:text-gray-900 whitespace-nowrap">
                    <i class="fas fa-couch mr-2"></i>Lounge Network
                </button>
                <button data-tab="merchants" class="tab-button px-4 py-3 font-medium transition-colors text-gray-600 hover:text-gray-900 whitespace-nowrap">
                    <i class="fas fa-shopping-bag mr-2"></i>Merchant Services
                </button>
                <button data-tab="cashflow" class="tab-button px-4 py-3 font-medium transition-colors text-gray-600 hover:text-gray-900 whitespace-nowrap">
                    <i class="fas fa-money-bill-wave mr-2"></i>Cash Flow Models
                </button>
                <button data-tab="analytics" class="tab-button px-4 py-3 font-medium transition-colors text-gray-600 hover:text-gray-900 whitespace-nowrap">
                    <i class="fas fa-chart-bar mr-2"></i>Analytics
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8">
        <!-- Tab Content Container -->
        <div id="tab-content">
            <!-- Relationships Tab Content -->
            <div id="relationships-tab" class="tab-panel active fade-in">
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <!-- AMEX Hub Card -->
                    <div class="lg:col-span-3">
                        <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                            <div class="flex flex-col md:flex-row items-center justify-between mb-8">
                                <div class="flex items-center space-x-4 mb-4 md:mb-0">
                                    <div class="bg-blue-600 p-4 rounded-xl text-white">
                                        <i class="fas fa-building text-3xl"></i>
                                    </div>
                                    <div>
                                        <h2 class="text-2xl font-bold text-gray-900">American Express</h2>
                                        <p class="text-blue-600 font-medium">Central Hub - 130M+ Cards Worldwide</p>
                                    </div>
                                </div>
                                <div class="flex space-x-4">
                                    <div class="text-center p-3 bg-blue-50 rounded-lg">
                                        <p class="text-xl font-bold text-blue-700">$42.4B</p>
                                        <p class="text-sm text-gray-600">Total Revenue</p>
                                    </div>
                                    <div class="text-center p-3 bg-green-50 rounded-lg">
                                        <p class="text-xl font-bold text-green-700">24.3%</p>
                                        <p class="text-sm text-gray-600">Travel Growth</p>
                                    </div>
                                </div>
                            </div>

                            <!-- Airlines Section -->
                            <div class="mb-8">
                                <h3 class="text-xl font-bold text-gray-900 mb-4 flex items-center">
                                    <i class="fas fa-plane mr-2 text-blue-600"></i>
                                    Airline Partners
                                </h3>
                                <div id="airlines-list" class="space-y-4">
                                    <!-- Airlines will be populated by JavaScript -->
                                </div>
                            </div>

                            <!-- Selected Airline Metrics -->
                            <div id="metrics-section" class="mb-8 hidden">
                                <h3 class="text-xl font-bold text-gray-900 mb-4 flex items-center">
                                    <i class="fas fa-chart-line mr-2 text-blue-600"></i>
                                    <span id="metrics-title">Metrics</span>
                                </h3>
                                <div id="metrics-container" class="grid grid-cols-2 md:grid-cols-4 gap-4">
                                    <!-- Metrics will be populated by JavaScript -->
                                </div>
                            </div>

                            <!-- Airport Relationships -->
                            <div>
                                <h3 class="text-xl font-bold text-gray-900 mb-4 flex items-center">
                                    <i class="fas fa-globe-americas mr-2 text-blue-600"></i>
                                    Airport Relationships
                                </h3>
                                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                                    <div class="bg-gray-50 rounded-lg p-4 card-hover">
                                        <h4 class="font-semibold text-gray-900 mb-2 flex items-center">
                                            <i class="fas fa-crown mr-2 text-purple-600"></i>
                                            Centurion Lounges
                                        </h4>
                                        <p class="text-sm text-gray-600 mb-2">40+ locations worldwide</p>
                                        <ul class="text-xs text-gray-600 space-y-1">
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> AMEX leases space from airports</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Premium experience for Platinum+ cardholders</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Drives card acquisition</li>
                                        </ul>
                                    </div>
                                    <div class="bg-gray-50 rounded-lg p-4 card-hover">
                                        <h4 class="font-semibold text-gray-900 mb-2 flex items-center">
                                            <i class="fas fa-users mr-2 text-blue-600"></i>
                                            Partner Lounges
                                        </h4>
                                        <p class="text-sm text-gray-600 mb-2">Delta Sky Clubs, Priority Pass</p>
                                        <ul class="text-xs text-gray-600 space-y-1">
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Access through co-branded cards</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> AMEX pays per-visit fees</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Enhances card value proposition</li>
                                        </ul>
                                    </div>
                                    <div class="bg-gray-50 rounded-lg p-4 card-hover">
                                        <h4 class="font-semibold text-gray-900 mb-2 flex items-center">
                                            <i class="fas fa-store mr-2 text-green-600"></i>
                                            Merchant Services
                                        </h4>
                                        <p class="text-sm text-gray-600 mb-2">Airport retailers & restaurants</p>
                                        <ul class="text-xs text-gray-600 space-y-1">
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Point-of-sale acceptance</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Merchant discount fees</li>
                                            <li><i class="fas fa-check text-green-500 mr-1"></i> Bonus categories for cardholders</li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Lounges Tab Content -->
            <div id="lounges-tab" class="tab-panel hidden fade-in">
                <div class="space-y-8">
                    <!-- Lounge Network Overview -->
                    <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                        <h2 class="text-2xl font-bold text-gray-900 mb-6 flex items-center">
                            <i class="fas fa-couch mr-3 text-purple-600"></i>
                            AMEX Global Lounge Network
                        </h2>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                            <div class="text-center p-6 lounge-tier rounded-xl text-white card-hover">
                                <i class="fas fa-crown text-4xl mb-4"></i>
                                <h3 class="text-xl font-bold mb-2">Centurion Lounges</h3>
                                <p class="text-3xl font-bold">40+</p>
                                <p class="text-purple-100">Locations Worldwide</p>
                            </div>
                            <div class="text-center p-6 bg-blue-600 rounded-xl text-white card-hover">
                                <i class="fas fa-users text-4xl mb-4"></i>
                                <h3 class="text-xl font-bold mb-2">Partner Lounges</h3>
                                <p class="text-3xl font-bold">1,300+</p>
                                <p class="text-blue-100">Priority Pass Locations</p>
                            </div>
                            <div class="text-center p-6 bg-green-600 rounded-xl text-white card-hover">
                                <i class="fas fa-plane text-4xl mb-4"></i>
                                <h3 class="text-xl font-bold mb-2">Airline Lounges</h3>
                                <p class="text-3xl font-bold">500+</p>
                                <p class="text-green-100">Delta Sky Clubs & More</p>
                            </div>
                        </div>

                        <!-- Lounge Financial Model -->
                        <div class="bg-gray-50 rounded-lg p-6 mb-6 card-hover">
                            <h3 class="text-xl font-bold text-gray-900 mb-4">Lounge Network Financial Model</h3>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div>
                                    <h4 class="font-semibold text-gray-900 mb-3 flex items-center">
                                        <i class="fas fa-money-bill-wave mr-2 text-green-600"></i>
                                        Revenue Streams
                                    </h4>
                                    <div class="space-y-3">
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Annual Card Fees</span>
                                            <span class="font-bold text-green-600">$2.1B</span>
                                        </div>
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Interchange on Lounge Spend</span>
                                            <span class="font-bold text-green-600">$180M</span>
                                        </div>
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Partner Revenue Sharing</span>
                                            <span class="font-bold text-green-600">$450M</span>
                                        </div>
                                    </div>
                                </div>
                                <div>
                                    <h4 class="font-semibold text-gray-900 mb-3 flex items-center">
                                        <i class="fas fa-receipt mr-2 text-red-600"></i>
                                        Cost Structure
                                    </h4>
                                    <div class="space-y-3">
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Lounge Operations</span>
                                            <span class="font-bold text-red-600">$1.2B</span>
                                        </div>
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Partner Access Fees</span>
                                            <span class="font-bold text-red-600">$650M</span>
                                        </div>
                                        <div class="flex justify-between items-center p-3 bg-white rounded-lg">
                                            <span>Real Estate Leases</span>
                                            <span class="font-bold text-red-600">$380M</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Lounge Access Matrix -->
                        <div class="mb-6 card-hover">
                            <h3 class="text-xl font-bold text-gray-900 mb-4">Lounge Access Matrix</h3>
                            <div class="overflow-x-auto bg-white rounded-lg shadow">
                                <table class="w-full">
                                    <thead class="bg-gray-100">
                                        <tr>
                                            <th class="px-4 py-3 text-left font-semibold">Card Type</th>
                                            <th class="px-4 py-3 text-center font-semibold">Centurion</th>
                                            <th class="px-4 py-3 text-center font-semibold">Delta Sky Clubs</th>
                                            <th class="px-4 py-3 text-center font-semibold">Priority Pass</th>
                                            <th class="px-4 py-3 text-center font-semibold">Guest Policy</th>
                                            <th class="px-4 py-3 text-center font-semibold">Annual Fee</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr class="border-b">
                                            <td class="px-4 py-3 font-medium">Platinum Card</td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center">2 Guests Free</td>
                                            <td class="px-4 py-3 text-center font-bold">$695</td>
                                        </tr>
                                        <tr class="border-b">
                                            <td class="px-4 py-3 font-medium">Delta Reserve</td>
                                            <td class="px-4 py-3 text-center text-red-600"><i class="fas fa-times"></i></td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center text-red-600"><i class="fas fa-times"></i></td>
                                            <td class="px-4 py-3 text-center">2 Guests Free</td>
                                            <td class="px-4 py-3 text-center font-bold">$550</td>
                                        </tr>
                                        <tr class="border-b">
                                            <td class="px-4 py-3 font-medium">Gold Card</td>
                                            <td class="px-4 py-3 text-center text-red-600"><i class="fas fa-times"></i></td>
                                            <td class="px-4 py-3 text-center text-red-600"><i class="fas fa-times"></i></td>
                                            <td class="px-4 py-3 text-center text-red-600"><i class="fas fa-times"></i></td>
                                            <td class="px-4 py-3 text-center">N/A</td>
                                            <td class="px-4 py-3 text-center font-bold">$250</td>
                                        </tr>
                                        <tr>
                                            <td class="px-4 py-3 font-medium">Centurion Card</td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center text-green-600"><i class="fas fa-check"></i></td>
                                            <td class="px-4 py-3 text-center">Unlimited Guests</td>
                                            <td class="px-4 py-3 text-center font-bold">$5,000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>

                        <!-- Lounge Partnership Details -->
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <!-- Centurion Lounges -->
                            <div class="bg-white border border-gray-200 rounded-lg p-6 card-hover">
                                <div class="flex items-center gap-3 mb-4">
                                    <div class="bg-purple-600 p-2 rounded-lg">
                                        <i class="fas fa-crown text-white"></i>
                                    </div>
                                    <h3 class="text-xl font-bold text-gray-900">Centurion Lounges</h3>
                                </div>
                                <div class="space-y-3">
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Locations</span>
                                        <span class="font-semibold">40+ worldwide</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Annual Visitors</span>
                                        <span class="font-semibold">4.2M</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Cost per Visitor</span>
                                        <span class="font-semibold">$85-125</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Cardholder Value</span>
                                        <span class="font-semibold">$550+ annually</span>
                                    </div>
                                </div>
                                <div class="mt-4 p-3 bg-purple-50 rounded-lg">
                                    <p class="text-sm text-purple-800">
                                        <strong>Business Model:</strong> AMEX operates directly, leases airport space, provides premium F&B. Drives $695+ annual fee justification.
                                    </p>
                                </div>
                            </div>

                            <!-- Delta Sky Clubs -->
                            <div class="bg-white border border-gray-200 rounded-lg p-6 card-hover">
                                <div class="flex items-center gap-3 mb-4">
                                    <div class="bg-blue-600 p-2 rounded-lg">
                                        <i class="fas fa-users text-white"></i>
                                    </div>
                                    <h3 class="text-xl font-bold text-gray-900">Delta Sky Clubs</h3>
                                </div>
                                <div class="space-y-3">
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Locations</span>
                                        <span class="font-semibold">50+ clubs</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">AMEX Visitors</span>
                                        <span class="font-semibold">3.1M annually</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Fee per Visit</span>
                                        <span class="font-semibold">$39-50</span>
                                    </div>
                                    <div class="flex justify-between">
                                        <span class="text-gray-600">Annual Contract</span>
                                        <span class="font-semibold">$150-200M</span>
                                    </div>
                                </div>
                                <div class="mt-4 p-3 bg-blue-50 rounded-lg">
                                    <p class="text-sm text-blue-800">
                                        <strong>Partnership:</strong> AMEX pays Delta per visit + annual minimum. Drives Delta Reserve card acquisition ($550 fee).
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Merchants Tab Content -->
            <div id="merchants-tab" class="tab-panel hidden fade-in">
                <div class="space-y-8">
                    <!-- Merchant Services Overview -->
                    <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                        <h2 class="text-2xl font-bold text-gray-900 mb-6 flex items-center">
                            <i class="fas fa-shopping-bag mr-3 text-green-600"></i>
                            Airport Merchant Services Network
                        </h2>

                        <!-- Merchant Financial Summary -->
                        <div class="grid grid-cols-1 md:grid-cols-4 gap-4 mb-8">
                            <div class="text-center p-4 merchant-tier rounded-xl text-white card-hover">
                                <p class="text-2xl font-bold">$28B</$28B</p>
                                <p class="text-sm">Annual Airport Spend</pp>
                                <p class="text-sm">Annual Airport Spend</p>
                            </div>
                           >
                            </div>
                            <div class="text-center p-4 bg-green-600 rounded <div class="text-center p-4-xl text-white card-hover">
                                <p class bg-green-600 rounded-xl text-white card-hover">
                                <p class="text-2="text-2xlxl font-bold">$840M</ font-bold">$840M</pp>
                                <p class="text-sm">AMEX Interchange</p>
                           >
                                <p class="text-sm">AMEX Interchange</p>
                            </div>
                            <div class=" </div>
                            <div class="text-center p-4 bg-blue-600 rounded-xl text-white card-hovertext-center p-4 bg">
                                <p class-blue-600 rounded-xl text-white card-hover">
                                <p="text-2xl font-bold">45%</p>
 class="text-2xl font-bold">45%</p>
                                <p class="text-sm                                <p class="text-sm">Market Share</p>
">Market Share</p>
                            </div>
                            <                            </div>
                            <div class="text-centerdiv class="text-center p- p-4 bg-purple4 bg-purple-600 rounded-xl text-white-600 rounded-xl text-white card-hover">
                                card-hover">
                                <p class="text-2xl <p class="text-2 font-bold">2.8Mxl font-bold">2.8M</p>
                                <p class="text-sm</p>
                                <p">Daily Transactions</p>
 class="text-sm">Daily Transactions</p>
                                                       </div>
                        </div>

                        <!-- Merchant Categories </div>
                        </div>

                        <!-- Merchant Categories -->
                        <div class="mb- -->
                        <div class="mb-8">
                           8">
                            <h3 <h3 class="text-xl font-bold text-gray class="text-xl font-bold text-gray--900 mb-900 mb-4">Mer4">Merchant Categorychant Category Analysis</h3 Analysis</h3>
>
                            <div class="                            <div class="grid gridgrid grid-cols--cols-1 md:1 md:grid-cols-3grid-cols-3 gap- gap-4">
4">
                                <div class="                                <div class="bg-gray-50 rounded-lg p-4 cardbg-gray-50 rounded-lg p-4-hover">
                                    card-hover">
                                    <div class="flex items-center <div class="flex items-center gap-2 mb gap-2 mb-3-3">
                                        <i class="">
                                        <i class="fas fa-utensilsfas fa-utensils text-orange-500"></ text-orange-500"></i>
                                        <i>
                                        <h4h4 class="font-semib class="font-semiboldold text-gray- text-gray-900900">Dining & Restaurants</">Dining & Restaurants</hh4>
4>
                                    </                                    </div>
                                    <div>
                                    <div class="space-y-2 textdiv class="space-y-2 text-sm">
                                        <div class="flex-sm">
                                        <div class="flex justify justify-between">
                                            <span>Annual-between">
                                            <span>Annual Volume</span>
                                            <span class Volume</span>
                                            <span class="font-semibold">$8="font-semibold">$8..4B</span>
                                        </div4B</span>
                                        </div>
                                        <div class="flex justify-between">
                                           >
                                        <div class="flex justify-between">
                                            < <span>AMEX Share</span>
                                            <spanspan>AMEX Share</span>
                                            <span class="font-semibold">38 class="font-semibold">38%</span>
                                        </%</span>
                                       div>
                                        <div class="flex </div>
                                        <div class=" justify-between">
                                            <spanflex justify-between">
                                            <span>>Interchange Rate</span>
                                            <span class="Interchange Rate</span>
                                            <span class="font-semibold">font-semibold">2.8%</2.8%</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>Bonus Points</span>
                                            <span class="font-semibold">5x Platinum</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="bg-gray-50 rounded-lg p-4 card-hover">
                                    <div class="flex items-center gap-2 mb-3">
                                        <i class="fas fa-shopping-cart text-blue-500"></i>
                                        <h4 class="font-semibold text-gray-900">Retail & Duty-Free</h4>
                                    </div>
                                    <div class="space-y-2 text-sm">
                                        <div class="flex justify-between">
                                            <span>Annual Volume</span>
                                            <span class="font-semibold">$12.2B</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>AMEX Share</span>
                                            <span class="font-semibold">42%</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>Interchangespan>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>Bonus Points</span>
                                            <span class="font-semibold">5x Platinum</span>
                                        </div>
                                    </div>
                                </div>

                                <div class="bg-gray-50 rounded-lg p-4 card-hover">
                                    <div class="flex items-center gap-2 mb-3">
                                        <i class="fas fa-shopping-cart text-blue-500"></i>
                                        <h4 class="font-semibold text-gray-900">Retail & Duty-Free</h4>
                                    </div>
                                    <div class="space-y-2 text-sm">
                                        <div class="flex justify-between">
                                            <span>Annual Volume</span>
                                            <span class="font-semibold">$12.2B</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>AMEX Share</span>
                                            <span class="font-semibold">42%</span>
                                        </div>
                                        <div class="flex justify-between">
                                            <span>Interchange Rate</ Rate</span>
                                            <span class="font-semibspan>
                                            <span classold">2.3%="font-semibold">2.3%</span</span>
                                        </>
                                        </div>
                                        <div>
                                        <div classdiv class="flex justify="flex justify-between">
                                           -between">
                                            <span> <span>Bonus Points</Bonus Points</span>
                                            <spanspan>
                                            <span class="font class="font-semibold">1-semibold">1x Standard</span>
                                       x Standard</span>
                                        </div>
                                    </div>
                                    </div>
                                </div>

                                <div class="bg-gray-50 rounded-lg </div>
                                </div>

                                <div class="bg-gray-50 rounded-lg p-4 card-hover p-4 card-hover">
                                    <div">
                                    <div class=" class="flex items-center gapflex items-center gap--2 mb-3">
2 mb-3">
                                                                               <i class="fas <i class="fas fa-car fa-car text-green-500 text-green-500"></i"></i>
                                        <h4 class="font-semibold text-gray-900">Services & Parking</h4>
                                    </div>
                                    <div class="space-y-2 text-sm">
                                       >
                                        <h4 class="font-semibold text-gray-900">Services & Parking</h4>
                                    </div>
                                    <div class="space-y-2 text-sm">
                                        <div class="flex justify-between">
                                            <span>Annual <div class="flex justify-between">
                                            <span>Annual Volume</span>
                                            <span Volume</span>
                                            <span class="font-semib class="font-semibold">$7.4B</span>
                                        </div>
                                        <div class="old">$7.4B</span>
                                        </div>
                                        <div class="flex justify-between">
                                           flex justify-between">
                                            <span>AMEX Share</span>
                                            <span class="font-semibold">35%</span>
                                        </div>
                                        <span>AMEX Share</span>
                                            <span class="font-semibold">35%</span>
                                        </div>
                                        < <div class="flex justify-between">
                                            <span>Interchange Rate</span>
                                            <span class="fontdiv class="flex justify-between">
                                            <span>Interchange Rate</span>
                                            <span class="font-semib-semiboldold">2">2..1%</span>
                                        </1%</span>
                                        </div>
                                       div>
                                        <div class="flex justify-between">
 <div class="flex justify-between">
                                            <span>Bonus Points                                            <span>Bonus Points</span>
                                            <span</span>
                                            <span class="font-semibold class="font-semibold">2x Gold</">2x Gold</span>
                                        </div>
                                   span>
                                        </div>
                                    </div>
                                </div </div>
                                </div>
                            </div>
                       >
                            </div>
                        </div>

                        </div>

                        <!-- Merchant Partnership Models -->
                        <div <!-- Merchant Partnership Models -->
                        <div class="mb-6">
 class="mb-6">
                            <h3 class="                            <h3 class="text-xl font-bold text-graytext-xl font-bold text-gray-900 mb--900 mb-4">Merchant Partnership Models</h4">Merchant Partnership Models</h3>
3>
                            <div class="grid grid-cols-                            <div class="grid grid-cols-1 md:grid-cols1 md:grid-cols-2 gap-6-2 gap-6">
">
                                <!-- Airport Con                                <!-- Airport Concessions -->
                                <div classcessions -->
                                <div class="bg-white border border-gray-="bg-white border border-gray200 rounded-lg p-6-200 rounded-lg p-6 card-hover">
                                    card-hover">
                                    <h4 class=" <h4 class="font-semibold text-grayfont-semibold text-gray-900 mb-900 mb-3-3 flex items-center">
                                        <i flex items-center">
                                        <i class="fas fa-building class="fas fa-building mr mr-2 text-blue--2 text-blue-600"></i>
                                        Airport Con600"></i>
                                        Airport Concession Agreements
                                    </hcession Agreements
                                    </h4>
                                    <div class4>
                                    <div class="space-y-3 text="space-y-3 text-sm">
                                       -sm">
                                        <div class="flex justify-between p- <div class="flex justify-between p-2 bg-gray-50 rounded2 bg-gray-50 rounded">
                                           ">
                                            <span>Term <span>Terminal POS Fees</span>
                                           inal POS Fees</span>
 <span class="font-sem                                            <span class="fontibold">0.15-semibold">0.-0.25%</15-0.25%span>
                                        </div>
</span>
                                        </div>
                                                                               <div class="flex justify-between p-2 <div class="flex bg-gray-50 rounded">
 justify-between p-2 bg-gray-50                                            <span rounded">
                                            <span>Minimum Annual>Minimum Annual Guar Guaranteeantee</</span>
span>
                                            <span class="                                            <span class="font-semibold">$font-semibold">$5-20M per major airport</span>
                                        </5-20M per major airport</span>
                                        </div>
                                        <div classdiv>
                                        <div class="flex justify-between p="flex justify-between p-2 bg-gray-50 rounded">
                                            <span>Technology Integration</-2 bg-gray-50 rounded">
                                            <span>Technology Integration</span>
                                            <span class="font-semibold">span>
                                            <span class="font-semibold">AMAMEX-funded</span>
                                        </div>
                                        <div classEX-funded</span>
                                        </div>
                                        <div class="flex justify-between p-2 bg="flex justify-between p-2 bg-gray-50 rounded">
                                            <span-gray-50 rounded">
                                           >Marketing Contributions</span>
 <span>Marketing Contributions</                                            <span class="fontspan>
                                            <span class-semibold">$2-5M annually</span="font-semibold">$2-5M annually>
                                        </div>
</span>
                                        </div>
                                    </div>
                                    </div>
                                </                                </div>

                                <!--div>

                                <!-- Airline Airline Merchant Services -->
                                Merchant Services -->
                                <div class="bg-white border <div class="bg-white border-gray-200 rounded-lg border border-gray-200 p-6 card-hover rounded-lg p-6 card-hover">
                                    <h">
                                    <h4 class4 class="font-semib="font-semiboldold text-gray-900 mb text-gray-900 mb-3-3 flex items-center">
                                        <i class="fas flex items-center">
                                        <i class="fas fa-plane fa-plane mr-2 text mr-2 text-green--green-600"></i>
600"></i>
                                        Air                                        Airline Co-Brandline Co-Brand Benefits
                                    </h4>
                                    Benefits
                                    </h4>
                                    <div class <div class="space-y="space-y-3-3 text-sm">
                                        text-sm">
                                        <div <div class="flex justify class="flex justify-between p-between p-2 bg-gray-50 rounded">
                                           -2 bg-gray-50 rounded">
                                            <span> <span>Bonus Mile Earnings</Bonus Mile Earnings</span>
                                           span>
                                            <span class <span class="font="font-semibold">-semibold">2-2-5x at partners</span>
                                        </div5x at partners</span>
                                        </div>
                                       >
                                        <div class="flex justify <div class="flex justify-between p-2 bg-gray-between p-2 bg-gray--50 rounded">
                                           50 rounded">
                                            <span>Partner Marketing</span>
                                            <span>Partner Marketing</span <span class="font-sem>
                                            <span class="ibold">Co-funded campaignsfont-semibold">Co-funded campaigns</span>
                                       </span>
                                        </div>
                                        <div class </div>
                                        <div class="flex justify="flex justify-between p-between p-2 bg-gray-50 rounded">
-2 bg-gray-50 rounded">
                                            <span>Revenue Sharing                                            <span>Revenue Sharing</span>
                                            <span class="font-sem</span>
                                            <span class="ibold">10font-semibold">10-25% of interchange</span-25% of interchange</span>
                                        </div>
>
                                        </div>
                                        <div class="flex                                        <div class="flex justify-between p-2 bg justify-between p-2 bg-gray-50 rounded">
                                           -gray-50 rounded">
                                            <span>Statement Credits</ <span>Statement Credits</span>
                                            <span classspan>
                                            <span="font-semib class="font-semibold">$100-200 airline feeold">$100-200 airline fee</span>
                                        </div</span>
                                        </div>
                                    </div>
                                    </div>
                                </div>
                           >
                                </div>
                            </div>
                        </ </div>
                        </div>
                    </div>
                </div>
                    </div>
                </div>
            </div>

div>
            </div>

            <!-- Cash Flow Tab Content            <!-- Cash Flow Tab Content -->
            <div id="cash -->
            <div id="flow-tab" classcashflow-tab"="tab-panel hidden fade class="tab-panel hidden fade-in">
                <div-in">
                <div class class="space-y-8="space-y-8">
                    <div id="">
                    <div id="cashflow-buttons" classcashflow-buttons" class="grid grid="grid grid-cols-1 md:grid-cols-cols-1 md:grid-c-2 lg:grid-cols-2 lg:gridols-4 gap--cols-4 gap-4 mb-6">
4 mb-6">
                                               <!-- Cash flow buttons <!-- Cash flow buttons will be populated by will be populated by JavaScript -->
                    </div>

                    JavaScript -->
                    </div>

 <div id="selected-flow-content"                    <div id="selected-flow-content" class="hidden class="hidden">
                        <!--">
                        <!-- Selected flow content Selected flow content will be will be populated by JavaScript -->
                    </div>

                    populated by JavaScript -->
                    </div>

                    <div id="no-flow-selected" class="bg-white rounded-xl shadow-lg p- <div id="no-flow-selected" class="bg-white rounded-xl shadow-lg p-12 text-center card-hover12 text-center card-hover">
                        <i class="">
                        <i class="fas fa-money-bill-wavefas fa-money-bill-wave text-6xl text-gray text-6xl text-gray-400 mx-auto mb--400 mx-auto mb-4"></i>
                       4"></i>
                        <p class="text <p class="text-gray--gray-600 text-xl">600 text-xl">Select a cash flow model above to see detailed breakdown</p>
                   Select a cash flow model above to see detailed breakdown</p>
                    </div </div>
                </div>
                </div>
            </div>

            <!-- Analytics Tab Content -->
            <div>
            </div>

            <!-- Analytics Tab Content -->
            <div id="analytics-tab" class="tab-panel hidden fade id="analytics-tab" class="tab-panel hidden fade-in">
                <div class-in">
                <div class="space-y-8">
="space-y-8">
                    <div class="grid                    <div class="grid grid-cols-1 lg grid-cols-1 lg:grid-cols-2:grid-cols-2 gap-8">
                        <!-- gap-8">
                        <!-- Partnership Performance -->
                        <div Partnership Performance -->
                        <div class="bg-white rounded-xl class="bg-white rounded-xl shadow-lg p-6 card shadow-lg p-6 card-hover">
                            <h-hover">
                            <h3 class="text-xl font3 class="text-xl font-bold text-gray--bold text-gray-900 mb-4 flex items900 mb-4 flex items-center-center">
                                <i class">
                                <i class="fas fa-chart-line="fas fa-chart-line mr-2 text-blue-600 mr-2 text-blue-600"></"></i>
                                Partnership Performancei>
                                Partnership Performance

                            </h3                            </h3>
                            <div id=">
                            <div id="partnership-performance" class="partnership-performance" class="space-y-4">
                               space-y-4">
                                <!-- Partnership performance will be populated by <!-- Partnership performance will be populated by JavaScript -->
                            </div JavaScript -->
                            </div>
                        </div>

                       >
                        </div>

                        <!-- Revenue Distribution -->
                        <!-- Revenue Distribution -->
                        < <div class="bg-white rounded-xl shadow-lg pdiv class="bg-white rounded-xl shadow-6 card-hover">
-lg p-6 card-h                            <h3 classover">
                            <h3 class="text-xl font-bold="text-xl font-bold text-gray-900 mb- text-gray-900 mb-4 flex4 flex items-center">
                                < items-center">
                                <i class="i class="fas fa-chart-pie mrfas fa-chart-pie-2 text-green-600"></ mr-2 text-green-600"></i>
                                Revenue Distribution
i>
                                Revenue Distribution
                            </h3>
                                                       </h3>
                            <div id="revenue <div id="revenue-distribution" class="space-distribution" class="space-y-3">
                               -y-3">
 <!-- Revenue distribution will be populated by                                <!-- Revenue distribution will be populated by JavaScript -->
                            </div>
 JavaScript -->
                            </div>
                        </div                        </div>
                    </>
                   div>

                    <!-- Key Metrics Dashboard -->
                    </div>

                    <!-- Key Metrics Dashboard -->
                    <div class="bg-white rounded-xl shadow <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                       -lg p-6 card-hover">
                        < <h3 class="text-xl font-boldh3 class="text-xl font-bold text-gray-900 mb- text-gray-900 mb-6 flex items-center">
                           6 flex items-center">
                            <i class=" <i class="fas fa-tachometer-altfas fa-tachometer-alt mr-2 text-purple- mr-2 text-purple-600"></i>
                            Key Partnership Metrics
                        </h3>
                       600"></i>
                            Key Partnership Metrics
                        </h3>
                        <div class=" <div class="grid grid-cgrid grid-cols-2ols-2 md:grid-c md:grid-cols-4 gap-4">
                           ols-4 gap-4">
                            <div class=" <div class="text-center ptext-center p-4-4 bg-blue-50 bg-blue-50 rounded-lg rounded-lg card-hover">
                                <p class card-hover">
                                <p class="text-="text-2xl font2xl font-bold text-blue-bold text-blue-600">12.5M</-600">12.5pM</p>
>
                                                               <p class <p class="="text-sm text-gray-text-sm text-gray-600">600">Delta CardholdersDelta Cardholders</p>
                            </div>
                            <</p>
                            </div>
                            <div class="text-center p-4div class="text-center p-4 bg-green-50 rounded-lg card-hover">
                                bg-green-50 rounded-lg card-hover">
                                <p class="text-2 <p class="text-2xl font-boldxl font-bold text-green-600">$3. text-green-600">$3.8B</p>
                                <p class="text-sm text8B</p>
                                <p class="text-sm text-gray-600">Miles-gray-600">Miles Sold to AM Sold to AMEX</pEX</p>
                           >
                            </div>
                            </div>
                            <div <div class="text-center p- class="text-center p-4 bg-purple-504 bg-purple-50 rounded-lg card-hover">
                                rounded-lg card-hover">
                                <p class="text <p class="text--2xl font-bold text2xl font-bold text-purple-600">8-purple-600">8.7M</p>
.7M</p>
                                <p class="text                                <p class="text-sm text-gray-600">-sm text-gray-600">Award RedAward Redemptions</emptionsp>
                            </div>
                            <</p>
                            </div>
                            <div class="text-center p-4 bg-ordiv class="text-center p-4 bg-orange-50 rounded-lg cardange-50 rounded-lg card-hover">
                                <p-hover">
                                <p class="text-2 class="text-2xlxl font-bold text-orange font-bold text-orange-600">2.1-600">2.1M</p>
                                <pM</p>
                                <p class="text-sm text-gray class="text-sm text-gray-600">Lounge-600">Lounge Visits</p>
                            </ Visits</p>
div>
                        </div>
                            </div>
                        </                    </div>
                </div>
            </div>
div>
                    </div>
                </div>
            </div>
        </div>
        </div>
    </main>

    <!-- Footer -->
    </main>

    <!-- Footer -->
    <footer class    <footer class="bg-gray-800 text="bg-gray-800 text-white py-8 mt-white py-8 mt-12">
        <div class-12">
        <div class="container="container mx-auto px- mx-auto px-4">
            <div class="grid4">
            <div class="grid grid-cols- grid-cols-1 md:grid-cols1 md:grid-cols-3 gap-8">
               -3 gap-8">
                <div <div>
                   >
                    <h3 class="text <h3 class="text-xl font-bold mb-4">-xl font-bold mb-4AMEX Partnership Ecosystem</h">AMEX Partnership Ecosystem</h3>
                    <p3>
                    <p class="text-gray-400"> class="text-gray-400">A comprehensive analysis of AmericanA comprehensive analysis of American Express airline Express airline partnerships, lounge partnerships, lounge networks, and merchant networks, and merchant services.</p>
                </div>
                < services.</p>
                </div>
div>
                    <h3 class                <div>
                    <h3 class="="text-xl font-bold mb-4">Data Sourcestext-xl font-bold mb-</h3>
                   4">Data Sources</h3>
                    <ul class="text-gray-400 space-y-2 <ul class="text-gray-400 space-y-2">
                        <li">
                        <li>AMEX Annual Reports</li>
                        <li>>AMEX Annual Reports</li>
                        <li>Airline Financial Disclosures</li>
Airline Financial Disclosures</li>
                        <li>Industry Analysis                        <li>Industry Analysis</li>
                        <li</li>
                        <li>Partnership Agreements</li>Partnership Agreements</li>
                    </>
                    </ulul>
                </div>
                </div>
                <div>
                    <h>
                <div>
                    <h3 class="text-xl font-bold mb3 class="text-xl font-bold mb-4">Updated</h3-4">Updated</h3>
                    <p class="text-gray-400>
                    <p class="text-gray-400">Last updated: March 2024</">Last updated: March 2024</p>
                    <div class="flex space-x-4 mtp>
                    <div class="flex space-x-4-4">
                        <a href="#" class="text-gray mt-4">
                        <a href="#" class="text-400 hover:text-white-gray-400 hover:text-white"><i class="fab fa-tw"><i class="fab fa-twitter"></i></a>
                        <a href="#" classitter"></i></a>
                        <a href="#" class="text-gray-="text-gray-400 hover:text-white"><i class="400 hover:text-white"><i class="fab fa-linkedin"></fab fa-linkedin"></ii></a>
                        <></a>
                        <aa href="#" class="text-gray-400 hover:text href="#" class="text-gray-400 hover:text-white"><i class="fab-white"><i class="fab fa-github"></i></ fa-github"></i></a>
a>
                    </div>
                </div>
            </div>
            <div                    </div>
                </div>
            </div>
            <div class="border-t border-gray- class="border-t border-gray-700 mt-8 pt-700 mt-8 pt-6 text-center text-gray-400">
                <p6 text-center text-gray-400">
                <p>>© 2024© 2024 AMEX Partnership Analysis. For educational purposes only.</p>
 AMEX Partnership Analysis. For educational purposes only.</p>
            </            </div>
        </div>
        </div>
   div>
    </footer>

    <script>
 </footer>

    <script>
        // Data models
        // Data models
        const airlines = [
            { 
        const airlines = [
            { 
                id: 'delta',
                name:                id: 'delta',
                name: 'Delta 'Delta Air Lines', 
                type: 'Primary Partner Air Lines', 
                type: 'Primary Partner', 
', 
                strength:                 strength: 100, 
                color: 'bg100, 
                color: 'bg-blue-600',
-blue-600',
                code                code: 'DAL'
            },
            { 
: 'DAL'
            },
            { 
                id                id: 'american',
: 'american',
                name: 'American Airlines', 
                type: 'Partner', 
                strength: 60, 
                color: 'bg-red-500',
                code: 'AAL'
            },
            {                name: 'American Airlines', 
                type: 'Partner', 
                strength: 60, 
                color: 'bg-red-500',
                code: 'AAL'
            },
            { 
                id: 'united',
                name: 'United Airlines', 
                type: 
                id: 'united',
                name: 'United Airlines', 
                type: ' 'Partner', 
                strength: 50, 
                colorPartner', 
                strength: 50, 
                color: 'bg-blue-: 'bg-blue-500500',
                code:',
                code: 'UAL'
            },
            { 'UAL'
            },
            { 
                id: 'jet 
                id: 'jetblue',
                name:blue',
                name: 'JetBlue', 
 'JetBlue', 
                               type: 'Partner', 
                strength:  type: 'Partner', 
                strength: 40, 
                color:40, 
                color: 'bg-indigo-500',
 'bg-indigo-500                code: 'JBLU'
            },
            { 
',
                code: 'JBLU'
            },
            { 
                id: 'south                id: 'southwest',
                name: 'Southwest', 
                typewest',
                name: 'Southwest', 
               : 'Limited Partner', 
                strength: 30, type: 'Limited Partner', 
                strength: 30, 
                color: ' 
                color: 'bgbg-orange-orange-500',
                code: 'LUV'
            }
        ];

        const financialMetrics = {
            delta: {
                annual: {
                    totalRevenue: 7.2,
                    cardholders: 12.5,
                    milesSold: 3.8,
                   -500',
                code: 'LUV'
            }
        ];

        const financialMetrics = {
            delta: {
                annual: {
                    totalRevenue: 7.2,
                    cardholders: 12.5,
                    milesSold: 3.8,
                    interchange: interchange: 1.2,
                    coBrandRevenue: 4 1.2,
                    coBrandRevenue: 4.5,
                    loungeVis.5,
                    loungeVisits: 2.1,
                    awardRedemptionsits: 2.1,
                    awardRedemptions: 8.7
: 8.7
                },
                quarterly: {
                },
                quarterly: {
                    totalRevenue: 1                    totalRevenue: 1.8,
                    card.8,
                    cardholders:holders: 12.5,
                    milesSold: 0 12.5,
                    milesSold: 0.95,
                    interchange.95,
                    interchange: 0.3,
                   : 0.3,
                    coBrandRevenue:  coBrandRevenue: 1.125,
                   1.125,
                    loungeVis loungeVisits:its: 0.525,
                    awardRed 0.525,
                    awardRedemptions: 2.175
               emptions: 2.175
                }
            },
            american: {
                annual: {
 }
            },
            american: {
                annual:                    totalRevenue: 2 {
                    totalRevenue: 2.8,
                    card.8,
                    cardholders: 4.2,
                    milesSold:holders: 4.2,
                    milesSold: 1.5,
                    interchange 1.5,
                   : 0.6,
                    interchange: 0.6,
                    coBrandRevenue: 1.8,
                    coBrandRevenue: 1.8,
                    loungeVisits: 0 loungeVisits: 0.8,
                    awardRed.8,
                    awardRedemptions: 3.2
                },
                quarterlyemptions: 3.2
                },
                quarterly: {
                    totalRevenue:: {
                    totalRevenue: 0.7,
                    cardholders: 4. 0.7,
                    cardholders: 4.2,
                    milesSold2,
                    milesSold: 0.375,
: 0.375,
                    interchange: 0                    interchange: 0.15,
                    coBrandRevenue.15,
                    coBrandRevenue: 0.45,
: 0.45,
                    loungeVisits:                     loungeVisits: 0.2,
                   0.2,
                    awardRedemptions: awardRedemptions: 0.8
                }
            },
            united: {
 0.8
                }
            },
            united: {
                annual: {
                    total                annual: {
                    totalRevenue:Revenue: 2.3,
                    cardholders:  2.3,
                    cardholders: 3.3.8,
                    milesSold: 1.28,
                    milesSold: 1.2,
                   ,
                    interchange: 0 interchange: 0.5,
                    coBrandRevenue: 1.5,
                   .5,
                    coBrandRevenue: 1.5,
                    loungeVisits: 0. loungeVisits: 06,
                    awardRed.6,
                    awardRedemptions: 2.8
                },
               emptions: 2.8
                },
                quarterly quarterly: {
                    totalRevenue:: {
                    totalRevenue: 0.575,
                    0.575,
                    cardholders: 3. cardholders: 3.8,
                    milesSold: 8,
                    milesSold: 0.3,
                   0.3,
                    interchange: 0.125,
                    coBrandRevenue: interchange: 0.125,
                    coBrandRevenue: 0.375,
                    loungeVis 0.375,
                    loungeVisitsits:: 0.15,
 0.15,
                                       awardRedemptions: 0.7
                }
            }
 awardRedemptions: 0.7
                }
            }
               };

        const cashFlows = [
            {
                id: ' };

        const cashFlows = [
            {
                id: 'tticket-purchase',
                title: 'icket-purchase',
                title: 'Ticket Purchase Flow',
                description: 'Direct flightTicket Purchase Flow',
                description: 'Direct flight booking transactions through AMEX cards',
                steps: booking transactions through AMEX cards',
                steps: [
                    { party: 'Cardholder', action: ' [
                    { party: 'Cardholder', action: 'Books flight using AMEX card', amount: '$500' },
Books flight using AMEX card', amount: '$500'                    { party: 'AMEX', action: ' },
                    { party: 'AMEX', action: 'Pays airline (minus interchange)', amount: '$490'Pays airline (minus interchange)', amount: '$490' },
                    { party: 'Airline', action: ' },
                    { party: 'Airline', action: 'Receives payment, books revenueReceives payment, books revenue', amount: '$490'', amount: '$490' },
                    { party: ' },
                    { party: 'AMEX', action: 'AMEX', action: 'ChargCharges cardholder', amount: '$500' },
                    { party: 'es cardholder', amount: '$500' },
                    { party:AMEX', action: 'E 'AMEX', action: 'Earns interchange fee', amount:arns interchange fee', amount: '$10 (2%)' '$10 (2%)' }
                ],
                insights: {
                    annualValue: ' }
                ],
                insights: {
                    annualValue: '~$15-20B~$15-20B in travel spend',
                    amexRevenue: '$300 in travel spend',
                    amexRevenue: '$300--700M interchange',
                    airlineBenefit: '700M interchange',
                    airlineBenefit: 'Immediate cash flowImmediate cash flow'
                }
            },
            {
               '
                }
            },
            {
                id: 'miles-purchase',
                title id: 'miles-purchase',
                title: ': 'Miles Purchase by AMEX',
                description:Miles Purchase by AMEX 'Bulk miles acquisition for cardholder rewards',
',
                description: 'Bulk miles acquisition for cardholder rewards',
                steps                steps: [
                    { party: 'AMEX', action:: [
                    { party: ' 'Bulk purchasesAMEX', action: 'B miles from airline', amount: '$2B/year' },
ulk purchases miles from airline', amount: '$2B/year' },
                    { party: 'Airline',                    { party: 'Airline', action: 'Sells action: 'Sells miles at miles at ~ ~1.5-2¢ per1.5-2¢ per mile', amount: 'Immediate cash' },
                    mile', amount: 'Immediate cash' },
                    { party: 'AMEX', { party: 'AMEX', action: 'Issues miles to cardholders action: 'Issues miles to (spend bonuses)', amount: 'Customer acquisition' },
 cardholders (spend bonuses)', amount: 'Customer acquisition' },
                    { party: '                    { party: 'CardCardholder', action:holder', action: 'Earns miles on card spend', 'Earns miles on card spend', amount: amount: '1- '1-3x per $1' },
                    { party3x per $1' },
                    { party: 'Airline', action: 'L: 'Airline', action: 'Liability on balance sheetiability on balance sheet until redeemed', amount: ' until redeemed', amount: 'Deferred revenue' }
                ],
                insights: {
                    annualDeValue: '$3.5ferred revenue' }
                ],
                insights: {
                    annualValue: '$3.5-4B with Delta alone',
                   -4B with Delta alone',
                    amexRevenue amexRevenue: 'Card fee revenue > $1: 'Card fee revenue > $1B',
                    airlineB',
                    airlineBenefit: '70-80%Benefit: '70-80% profit margins'
                profit margins'
                }
            }
            },
            {
                id: 'redemption',
 },
            {
                id: 'redemption',
                title                title: 'Miles: 'Miles Redemption Flow',
                description Redemption Flow',
                description: 'Cardholder reward redemption: 'Cardholder reward redemption process',
 process',
                steps: [
                    { party: 'Card                steps: [
                    { party: 'Cardholder', action: 'Redeems miles for award ticketholder', action: 'Redeems miles for award ticket',', amount: '25K amount: '25K-50-50K miles' },
                    { party: 'Airline', action:K miles' },
                    { party: 'Airline', action: 'Provides seat ( 'Provides seat (marginal cost)', amount: '$50-100' },
                    { partymarginal cost)', amount: '$50-100' },
                    { party: 'Airline: 'Airline', action: 'Clears liability from books', amount: 'Revenue recognition' },
                    { party: 'Airline', action: 'Clears liability from books', amount: 'Revenue recognition' },
                    { party: 'Airline', action: 'Net profit per redemption', action: 'Net profit', amount: '$200-400' },
                    { party per redemption', amount: '$200-400' },
                    { party: 'AMEX: 'AMEX', action:', action: ' 'Customer loyalty maintained', amountCustomer loyalty maintained', amount: 'Retention value' }
                ],
                insights: {
: 'Retention value' }
                ],
                insights: {
                    annualValue: '8-                    annualValue: '8-10M award tickets',
                   10M award tickets',
                    amexRevenue: 'Increased card amexRevenue: 'Increased card retention retention',
                    airlineBenefit: '$375 avg profit per',
                    airlineBenefit: '$375 avg profit per redemption'
                }
            },
            {
                id: ' redemption'
                }
            },
            {
                id: 'cobrand',
                titlecobrand',
                title: 'Co-Brand: 'Co-Branded Carded Card Revenue',
                description: 'Partnership credit card Revenue',
                description: 'Partnership credit card economics',
                economics steps: [
                    { party: 'Cardholder', action: 'Applies',
                steps: [
                    { party: 'Cardholder', action: 'Applies for Delta SkyMiles AM for Delta SkyMiles AMEX', amount: '$0EX', amount: '$-550 annual fee' },
                    { party: 'AM0-550 annual fee' },
                    { party: 'AMEX', action: 'EX', action: 'Issues card, pays acquisition bonus', amountIssues card, pays acquisition bonus', amount: '70: '70K-K-100K miles' },
                    { party: 'Delta100K miles' },
                    { party: 'Delta', action', action: 'Rece: 'Receives payment forives payment for miles', amount: '$1,400-2,000' },
 miles', amount: '$1,400-2,000' },
                    { party:                    { party: 'Cardholder', action: ' 'Cardholder', action: 'Spends on card annuallySpends on card annually', amount: '$15,', amount: '$15,000 avg' },
                    {000 avg' },
                    { party: 'AMEX', action party: 'AMEX', action: 'Shares: 'Shares interchange with Delta', amount: '50% interchange with Delta', amount: '50% split (~$225 split (~$225)' }
)' }
                ],
                insights: {
                    annualValue:                ],
                insights: {
                    annualValue: 'Delta 'Delta: $4-6B, AMEX: $4-6B, AMEX: $2: $2-3B',
                    amexRevenue:-3B',
                    am 'Interchange + annual fees',
                    airlineBenefit:exRevenue: 'Interchange 'Most profitable "route" + annual fees',
                    airlineBenefit: 'Most profitable "route"'
                }
            }
        ];

        // State
'
                }
            }
        ];

        // State
        let state        let state = {
 = {
                       activeTab: 'relationships',
            selectedFlow: null,
            activeTab: 'relationships',
            selectedFlow: null,
            selectedAir selectedAirline: 'Delta Air Lines',
            timeframe: 'annual'
        };

line: 'Delta Air Lines',
            timeframe: 'annual'
        };

        // Utility functions
        function        // Utility functions
        function formatNumber(value, formatNumber(value, type = 'currency') {
            if (type === ' type = 'currency') {
currency') {
                return `            if (type === 'currency') {
                return `$${value}B`;
            }$${value}B`;
            } else if else if (type === 'count (type === 'count') {
                return `${value}M`;
            }
            return value;
        }

') {
                return `${value}M`;
            }
            return value;
        }

        function        function showTab(tabName) {
 showTab(tabName) {
            // Hide all tab panels
            document.querySelectorAll('.tab-p            // Hide all tab panels
            document.querySelectorAll('.tab-panel').forEach(panelanel').forEach(panel => {
                panel.classList.add(' => {
                panel.classList.add('hidden');
                panel.classList.remove('active');
           hidden');
                panel.classList });
            
            // Show selected tab panel
            document.getElementById.remove('active');
            });
            
            // Show selected tab panel
            document.getElementById(`${tabName}-tab`(`${tabName}-tab`).classList.remove('hidden).classList.remove('hidden');
            document.getElementById(`${tabName}-tab`');
            document.getElementById(`${tabName}-tab`).classList.add('active');
            
            // Update tab buttons
).classList.add('active');
            
            // Update tab buttons
            document.querySelectorAll('.            document.querySelectorAll('.tab-button').forEach(button => {
tab-button').forEach(                button.classList.remove('tab-active');
                button.classList.add('text-gray-600button => {
                button.classList.remove('tab-active');
                button.classList.add('text-gray-600', 'hover:text', 'hover:text-gray-900');
            });
            
           -gray-900');
            });
            
            document.querySelector(`[data-tab="${tab document.querySelector(`[dataName}"]`).classList.add('tab-active');
-tab="${tabName}"]`).classList.add('tab-active');
            document.querySelector            document.querySelector(`(`[data-tab="${tabName}"]`).[data-tab="${tabName}"]`).classList.remove('text-gray-600classList.remove('text-gray', 'hover:text-gray-900');
            
            // Update-600', 'hover:text-gray-900');
 state
            state.activeTab = tabName;
            
            // Update state
            state.activeTab = tabName;
        }

        function select        }

        function selectAirline(airlineAirline(airlineName)Name) {
            state.selectedAirline = airline {
            state.selectedAirline = airlineName;
            updateMetrics();
            updateAirlinesUI();
       Name;
            updateMetrics();
            updateAirlinesUI();
        }

        }

        function selectFlow(flowId) {
            state function selectFlow(flowId.selectedFlow = flowId;
            updateCashFlowUI();
) {
            state.selectedFlow = flowId;
            update        }

        function updateTimeframe(timeframe) {
           CashFlowUI();
        }

        function updateTimeframe(timeframe) {
            state.timeframe = timeframe;
            update state.timeframe = timeframe;
            updateMetrics();
        }

Metrics();
        }

        // UI Rendering Functions
        // UI Rendering Functions
        function renderAirl        function renderAirlines() {
            const containerines() {
            const container = document.getElementById('air = document.getElementById('airlines-list');
            container.innerHTML =lines-list');
            container.innerHTML = '';
            
            airlines '';
            
            airlines.forEach(airline => {
                const.forEach(airline => {
                const isSelected = state.selectedAirline === airline.name;
                isSelected = state.selectedAirline === airline.name;
                const revenue = airline.name === 'Delta Air const revenue = airline.name === Lines' ? '$7.2B/year' : 'Delta Air Lines' ? '$7.2B/year' : 
 
                                                             airline airline.name === 'American Airlines' ? '$2.name === 'American Airlines' ? '$2.8B/year' : 
                               airline.8B/year' : 
                               airline.name === 'United Airlines' ? '$2..name === 'United Airlines' ? '$2.3B/year' :3B/year' : '$0.5-1.5B/year';
                
                const airlineElement '$0.5-1.5B/year';
                
                const airlineElement = document = document.createElement('div');
                airlineElement.className =.createElement('div');
                airlineElement.className = `airline-item bg-gray-50 rounded `airline-item bg-gray-50 rounded-lg p-4 hover:shadow-md transition-lg p-4 hover:shadow-md transition-all cursor-pointer ${-all cursor-pointer ${isSelected ? 'ring-2 ringisSelected ? 'ring-2 ring-blue-500-blue-500' : ''' : ''}`;
                airlineElement.onclick = ()}`;
                airlineElement.onclick = () => selectAirline(airline.name);
 => selectAirline(                
                airlineElement.innerHTML = `
                    <div class="airline.name);
                
                airlineElement.innerHTML = `
                    <div class="flex itemsflex items-center justify-between mb-2">
                        <div-center justify-between mb-2">
                        <div class=" class="flex items-center gap-3">
                            <flex items-center gap-3">
                            <div class="wdiv class="w-3 h-3 rounded-full-3 h-3 rounded-full ${airline.color ${airline.color}"></div>
                            <span class="}"></div>
                            <span class="font-semibfont-semibold text-gray-900">${airline.name}</span>
                            <old text-gray-900">${airline.name}</span>
                            <span class="text-sm text-grayspan class="text-sm text-gray-600 bg-gray-600 bg-gray-200 px-2 py-1-200 px-2 py-1 rounded">${airline rounded">${airline.type.type}</span>
                            <span class="text-xs text-gray}</span>
                            <span class="text-xs text-gray-500 font-mono">-500 font-mono">${airline.code}</span>
                        </div>
${airline.code}</span>
                        </div>
                                               <span class="text-sm font-medium text-gray- <span class="text-sm font-medium text-gray-700">${revenue}</700">${revenue}</span>
                    </div>
span>
                    </div>
                    <div class="                    <div class="w-full bg-gray-200 rounded-full h-2">
w-full bg-gray-200                        <div class="h-2 rounded-full ${air rounded-full h-2">
                        <div class="h-2 rounded-full ${airline.color}" style="widthline.color}" style="width: ${airline.strength}%"></: ${airline.strength}%"></div>
                    </div>
                    ${div>
                    </div>
                    ${airline.name === 'Deltaairline.name === 'Delta Air Lines' ? `
                        <div class="mt- Air Lines' ? `
2 text-sm text-gray-                        <div class="mt-2 text-sm text-gray-600 bg-blue-50 p-2 rounded">
                            <strong>Exclusive600 bg-blue-50 p-2 partnership:</strong> Delta SkyMiles cards, lounge access rounded">
                            <strong>Exclusive partnership:</strong> Delta SkyMiles cards, lounge access, elite status benefits, elite
                        </div>
                    ` : ''}
                `;
                
 status benefits
                        </div>
                    ` : ''}
                `;
                
                container.appendChild(airline                container.appendChild(airlineElement);
            });
        }

        function updateMetrics()Element);
            });
        }

        function updateMetrics() {
            const airlineData = airlines.find {
            const airlineData(a => a.name === state.selectedAirline);
            = airlines.find(a => a.name === state.selectedAirline);
            if (!airline if (!airlineData || !financialMetrics[airlineData.id]) return;
            
Data || !financialMetrics[airlineData.id]) return;
            
            const            const metrics metrics = financialMetrics = financialMetrics[air[airlineData.idlineData.id][state.timeframe][state.timeframe];
            const];
            const metricsSection = document.getElementById('metrics-section');
            const metricsSection = document.getElementById('metrics-section');
            const metricsContainer = document.getElementById metricsContainer = document.getElementById('metrics-container');
            const metricsTitle = document.getElementById('metrics-title');
            
            metricsTitle.text('metrics-container');
            const metricsTitle = document.getElementById('metrics-title');
            
            metricsTitle.textContent = `${stateContent = `${state.selectedAirline} Partnership Metrics (${state.timeframe ===.selectedAirline} Partnership Metrics (${state.timeframe === 'annual' ? 'Annual' 'annual' ? 'Annual' : 'Quarterly'})`;
            metricsContainer.innerHTML : 'Quarterly'})`;
            metricsContainer.innerHTML = '';
            
            // Create metric = '';
            
            // Create metric cards
            const metricCards = [
                cards
            const metricCards = [
                { title: 'Total Revenue { title: 'Total Revenue', value', value: metrics.totalRevenue, type: 'currency',: metrics.totalRevenue, type: 'currency', change:  change: 5.2 },
                { title5.2 },
                { title: 'Cardholders', value: metrics: 'Cardholders', value: metrics.cardholders, type: 'count',.cardholders, type: 'count', change change: 3.8 },
                { title: 'Miles Sold', value: metrics.milesSold, type: 3.8 },
                { title: 'Miles Sold', value: metrics.milesSold, type: ': 'currency', change: 7.1 },
                { title:currency', change: 7.1 },
                { title: ' 'Interchange', value: metrics.interchange, typeInterchange', value: metrics.interchange, type: ': 'currency', change: 4.5 }
           currency', change: 4.5 }
            ];
            
            metricCards.forEach(metric => {
 ];
            
            metricCards.forEach(metric => {
                const metric                const metricCard = documentCard = document.createElement('div');
                metricCard.className =.createElement('div');
                metricCard.className = 'metric 'metric-card bg-white rounded-lg p-4 shadow-sm border border-gray-200-card bg-white rounded-lg p-4 shadow-sm border border';
                
                metricCard.innerHTML = `
                    <div-gray-200';
                
                metricCard.innerHTML = `
                    class="flex items-center justify-between mb-2 <div class="flex items-center justify-between mb-2">
                        <div class="flex items-center gap-">
                        <div class="flex items-center gap-2">
                            <i class="fas ${2">
                            <i class="fas ${metric.title === 'metric.title === 'Total Revenue' ? 'fa-dollar-signTotal Revenue' ? 'fa-dollar-sign'' : 
                                            metric : 
                                            metric.title === 'Cardholders' ? 'fa.title === 'Cardholders' ? 'fa-users' : 
                                            metric.title === 'Miles-users' : 
                                            metric.title === 'Miles Sold' ? Sold' ? 'fa-chart-line' 'fa-chart-line' : 'fa-credit-card'} 
                               text-blue-600"></ : 'fa-credit-card'} 
                               text-blue-i>
                            <span class="text-sm font-medium text600"></i>
                            <span class="text-sm font-gray-600">${metric.title}</span>
                       -medium text-gray-600">${metric.title}</span>
                        </div>
                        </div>
                        <span class="text-xs font-medium ${metric.change > 0 <span class="text-xs font-medium ${metric.change > 0 ? 'text-green- ? 'text-green-600' : 'text-red600' : 'text-red-600'}">
                            ${metric.change > 0-600'}">
                            ${metric.change > 0 ? '+' : ''}${metric ? '+' : ''}${metric.change}%
                        </.change}%
                        </span>
                    </divspan>
                    </div>
>
                    <p class="                    <p class="text-2xl font-bold text-graytext-2xl font-bold text-gray-900">${formatNumber(metric-900">${formatNumber(metric.value, metric.type)}</p>
                `;
                
                metricsContainer.appendChild.value, metric.type)}</p>
                `;
                
                metrics(metricCard);
            });
            
            metricsSection.classListContainer.appendChild(metricCard);
            });
            
            metricsSection.classList.remove('hidden');
        }

.remove('hidden');
        }

        function updateAirlines        function updateAirlinesUI() {
            renderUI() {
            renderAirlines();
            updateMetrics();
        }

        function renderCashAirlines();
            updateMetrics();
        }

        function renderCashFlowButtons() {
FlowButtons() {
            const container = document.getElementById('cash            const container = document.getElementById('cashflow-buttons');
flow-buttons');
            container.innerHTML = '';
            
            cashFlows.forEach            container.innerHTML = '';
            
            cashFlows.forEach(flow => {
                const is(flow => {
                const isSelected = stateSelected = state.selectedFlow === flow.id;
.selectedFlow === flow.id;
                const button = document.createElement('                const button = document.createElement('button');
                button.className = `button');
                button.className = `p-4 rounded-lg text-left transition-all cardp-4 rounded-lg text-left transition-all card-hover $-hover ${
                    isSelected
                       {
                    isSelected
                        ? 'bg-blue-600 text-white shadow-lg transform scale-105'
                        : ' ? 'bg-blue-600 text-white shadow-lg transform scale-105'
                        : 'bg-white text-gray-900bg-white text-gray-900 hover:shadow-md hover:shadow-md'
                }`;
'
                }`;
                button.onclick = () => selectFlow(flow.id);
                
                button.innerHTML = `
                button.onclick = () => selectFlow(flow.id);
                
                                   <h3 class="font-bold mb-2">${flow.title}</ button.innerHTML = `
                    <h3 class="font-bold mb-2">${flow.title}</h3>
                    <p class="text-sm opacity-h3>
                    <p class="text-sm opacity-80">${flow.description}</p>
                `;
                
                container80">${flow.description}</p>
                `;
                
                container.appendChild(button);
.appendChild(button);
            });
        }

        function updateCashFlowUI() {
            render            });
        }

        function updateCashFlowUI() {
            renderCashFlowCashFlowButtons();
            
            const selectedFlowContent = documentButtons();
            
            const selectedFlowContent = document.getElementById('.getElementById('selected-flow-content');
            const noFlowSelected = document.getElementById('no-flow-selected');
selected-flow-content');
            const noFlowSelected = document.getElementById('no-flow-selected');
            
            if (state.selected            
            if (state.selectedFlow) {
                const flow = cashFlows.findFlow) {
                const flow = cashFlows.find(f => f.id === state.selectedFlow);
                selectedFlowContent.classList.remove('hidden');
                noFlowSelected.classList.add('hidden');
                
                selectedFlowContent.innerHTML = `
                    <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                        <div class="flex items-center justify-between mb-6">
                            <h3 class="text-2xl font-bold text-gray-900">${flow.title}</h3>
                            <span class="text-sm text-gray-500">${flow.description}</span>
                        </div>
                        
                        <div class="space-y-4">
                            ${flow.steps.map((step, idx) => `
                                <div class="flow(f => f.id === state.selectedFlow);
                selectedFlowContent.classList.remove('hidden');
                noFlowSelected.classList.add('hidden');
                
                selectedFlowContent.innerHTML = `
                    <div class="bg-white rounded-xl shadow-lg p-6 card-hover">
                        <div class="flex items-center justify-between mb-6">
                            <h3 class="text-2xl font-bold text-gray-900">${flow.title}</h3>
                            <span class="text-sm text-gray-500">${flow.description}</span>
                        </div>
                        
                        <div class="space-y-4">
                            ${flow.steps.map((step, idx) => `
                                <div class="flow-step relative">
                                    <div class="flex items-start gap-4">
                                       -step relative">
                                    <div class="flex items-start gap-4">
                                        <div class="flex-shrink-0 w-8 h- <div class="flex-shrink-0 w-8 h-8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold">
                                            ${idx + 1}
                                        </div>
                                        <div class="flex-1 bg8 bg-blue-600 text-white rounded-full flex items-center justify-center font-bold">
                                            ${idx + 1}
                                        </div>
                                        <div class="flex-1 bg-gray-50 rounded-lg p-4">
-gray-50 rounded-lg p-4">
                                            <div class="flex items-center justify-between mb-2">
                                                                                           <div class="flex items-center justify-between mb-2">
                                                <span class="font-semibold text-blue- <span class="font-semibold text-blue600">${step.party}</span>
                                                <span class="text-sm font-600">${step.party}</span>
                                                <span class="text-sm font-bold text-green-600">${step.amount}</span>
-bold text-green-600">${step.amount}</span>
                                            </div>
                                            <p class="text-gray-700">${                                            </div>
                                            <p class="step.action}</p>
                                        </div>
                                    </div>
                               text-gray-700">${step.action}</p>
                                        </div>
                                    </div>
                                </div </div>
                            `).join('')}
                        </div>

                       >
                            `).join('')}
                        </div <div class="mt-6 bg-blue-50 rounded-lg>

                        <div class="mt-6 bg-blue-50 rounded-lg p-4">
 p-4">
                            <h4 class="font-semibold text                            <h4 class="font-semibold text-gray-900 mb-3 flex items-center">
                                <-gray-900 mb-3 flex items-center">
                                <ii class="fas fa-chart-bar mr-2 class="fas fa-chart-bar mr-2 text-blue-600"></i>
 text-blue-600"></                                Financial Impact Analysis
                            </h4>
                           i>
                                Financial Impact Analysis
                            </h4>
                            <div class="grid grid <div class="grid grid-cols-1 md:grid-cols-3 gap--cols-1 md:grid-cols-3 gap4 text-sm">
                                <div>
                                   -4 text-sm">
                                <div>
                                    <p class="font-semibold text-gray-700"> <p class="font-semibold text-gray-700">Annual Scale</p>
                                    <Annual Scale</p>
                                    <p class="text-grayp class="text-gray--600">${flow.insights.annualValue}</p>
                                </div>
600">${flow.insights.annualValue}</p>
                                </div>
                                <div>
                                <div>
                                    <p class="font-semibold text-gray-                                    <p class="font-semibold text-gray-700">AMEX Benefit</p700">AMEX Benefit</p>
                                    <p class="text-gray-600">${flow.>
                                    <p class="text-gray-600">${flow.insights.amexRevenue}</p>
                                </divinsights.amexRevenue}</p>
                                </div>
>
                                <div>
                                    <p class="font-semibold text-gray-700">Airline Benefit</p>
                                <div>
                                    <p class="font-semibold text-gray-700">Airline Benefit</p>
                                    <p class="text-gray-600">${flow.insights.airlineBenefit}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                `;
            } else {
                selectedFlowContent.classList.add('hidden');
                noFlowSelected.classList.remove('hidden');
            }
        }

        function renderPartnershipPerformance() {
            const container = document.getElementById('partnership-performance');
            container.innerHTML = '';
            
            airlines.forEach(airline => {
                const performanceElement = document.createElement('div');
                performanceElement.className = 'flex items-center justify-between p-3 bg-gray-50 rounded-lg';
                
                const revenue = airline.name === 'Delta Air Lines' ? '$7.2B' :
                              airline.name ===                                    <p class="text-gray-600">${flow.insights.airlineBenefit}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                `;
            } else {
                selectedFlowContent.classList.add('hidden');
                noFlowSelected.classList.remove('hidden');
            }
        }

        function renderPartnershipPerformance() {
            const container = document.getElementById('partnership-performance');
            container.innerHTML = '';
            
            airlines.forEach(airline => {
                const performanceElement = document.createElement('div');
                performanceElement.className = 'flex items-center justify-between p-3 bg-gray-50 rounded-lg';
                
                const revenue = airline.name === 'Delta Air Lines' ? '$7.2B' :
                              airline.name === 'American Airlines 'American Airlines' ? '$2.8B' :
                              airline.name === 'United' ? '$2.8B' :
                              airline.name === 'United Airlines' ? '$2.3B' : '$0.5-1.5B';
                
                Airlines' ? '$2.3B' : '$0.5-1.5B';
                
                performanceElement performanceElement.innerHTML = `
                    <div class="flex items-center gap-3">
                        <div.innerHTML = `
                    <div class="flex items-center gap-3">
                        <div class="w- class="w-3 h-3 rounded-full ${airline.color}"></div>
                        <span class="font-medium">${airline.name}</span>
                    </div>
                    <div class="text-right">
                        <p class="font-bold text-gray-900">${revenue}</p>
                        <p class="text-sm text-green-600">+${airline.strength / 10}% YoY</p>
                    </div>
                `;
                
                container.appendChild(performanceElement);
            });
        }

        function renderRevenueDistribution() {
            const container = document.getElementById('revenue-distribution');
            container.innerHTML = '';
            
            const revenueItems = [
                { label: 'Co-brand Cards', value: 45, color: 'bg-blue-500' },
               3 h-3 rounded-full ${airline.color}"></div>
                        <span class="font-medium">${airline.name}</span>
                    </div>
                    <div class="text-right">
                        <p class="font-bold text-gray-900">${revenue}</p>
                        <p class="text-sm text-green-600">+${airline.strength / 10}% YoY</p>
                    </div>
                `;
                
                container.appendChild(performanceElement);
            });
        }

        function renderRevenueDistribution() {
            const container = document.getElementById('revenue-distribution');
            container.innerHTML = '';
            
            const revenueItems = [
                { label: 'Co-brand Cards', value: 45, color: 'bg-blue-500' },
                { label: 'Miles Sales', value: 30, color: 'bg-green-500' },
                { label: 'Interchange', value: 15, color: 'bg-purple-500' },
                { label: 'Annual Fees', value: 10, color: 'bg-orange-500' }
            ];
            
            revenueItems.forEach(item => {
                const revenueElement = document.createElement('div');
                revenueElement.className = 'flex items-center justify-between';
                
                revenueElement.innerHTML = `
                    <div class="flex items-center gap-2">
                        <div class="w-3 h-3 rounded-full ${item.color}"></div>
                        <span class="text-sm font-medium">${item.label}</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <div class="w-32 bg-gray-200 rounded-full h-2">
                            <div class="h-2 rounded-full ${item.color}" style="width: ${item.value}%"></div>
                        </div>
                        <span class="text-sm font-bold w-8">${item.value}%</span>
                    </div>
                `;
                
                container.appendChild(revenueElement);
            });
        }

        // Initialize the application
        function init() {
            // Set up event listeners
            document.querySelectorAll('.tab-button').forEach(button => {
                button.addEventListener('click', (e) => {
                    const tabName = e.target.getAttribute('data-tab');
                    showTab(tabName);
                });
            });
            
            document.getElementById('timeframe-selector').addEventListener('change', (e) => {
                updateTimeframe(e.target.value);
            });
            
            // Initial render
            renderAirlines();
            updateMetrics();
            renderCashFlowButtons();
            { label: 'Miles Sales', value: 30, color: 'bg-green-500' },
                { label: 'Interchange', value: 15, color: 'bg-purple-500' },
                { label: 'Annual Fees', value: 10, color: 'bg-orange-500' }
            ];
            
            revenueItems.forEach(item => {
                const revenueElement = document.createElement('div');
                revenueElement.className = 'flex items-center justify-between';
                
                revenueElement.innerHTML = `
                    <div class="flex items-center gap-2">
                        <div class="w-3 h-3 rounded-full ${item.color}"></div>
                        <span class="text-sm font-medium">${item.label}</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <div class="w-32 bg-gray-200 rounded-full h-2">
                            <div class="h-2 rounded-full ${item.color}" style="width: ${item.value}%"></div>
                        </div>
                        <span class="text-sm font-bold w-8">${item.value}%</span>
                    </div>
                `;
                
                container.appendChild(revenueElement);
            });
        }

        // Initialize the application
        function init() {
            // Set up event listeners
            document.querySelectorAll('.tab-button').forEach(button => {
                button.addEventListener('click', (e) => {
                    const tabName = e.target.getAttribute('data-tab');
                    showTab(tabName);
                });
            });
            
            document.getElementById('timeframe-selector').addEventListener('change', (e) => {
                updateTimeframe(e.target.value);
            });
            
            // Initial render
            renderAirlines();
            updateMetrics();
            renderCashFlowButtons();
 renderPartnershipPerformance();
            renderRevenueDistribution();
        }

        // Start the application when DOM is loaded
                   renderPartnershipPerformance();
            renderRevenueDistribution();
        }

        // Start the application when DOM is loaded
 document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
