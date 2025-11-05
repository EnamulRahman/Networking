Routing
Definition

Routing is the process of determining the best path for data to travel from a source device to a destination device across one or more networks.

How It Works

Data leaves Computer 1 and is sent to a Router.

The router examines the destination IP address and decides whether to send it through Network 1 (Net1) or Network 2 (Net2).

The data may pass through multiple routers and networks before reaching Computer 2.

Routers use routing tables to make these decisions, ensuring data takes the most efficient and reliable route.

Purpose of Routing

Optimizes network performance

Ensures reliable data delivery across complex infrastructures

Improves application performance and responsiveness

Supports scalability as networks grow

Types of Routing

1. Static Routing

Routes are manually configured by an administrator.

Uses fixed paths that do not change automatically.

Advantages: Simple, predictable, and secure.

Disadvantages: Not scalable, difficult to maintain in large or changing networks.

Best for: Small, stable networks with few routers.

2. Dynamic Routing

Routes are automatically determined and updated using routing protocols.

Adapts to network changes (e.g., link failures or congestion).

Advantages: Scalable, self-adjusting, and efficient.

Disadvantages: More complex and requires additional resources.

Best for: Large, complex, or constantly changing networks.

Common Routing Protocols

OSPF (Open Shortest Path First)

A link-state routing protocol used within large organizations.

Calculates the shortest and most efficient path based on link cost.

Quickly updates when network changes occur.

Commonly used for internal routing (IGP – Interior Gateway Protocol).

BGP (Border Gateway Protocol)

A path-vector protocol used between large networks or ISPs.

Determines the best path across the internet.

Used for external routing (EGP – Exterior Gateway Protocol).

Ensures global data delivery between autonomous systems (AS).
