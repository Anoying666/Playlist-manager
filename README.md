🎶 Playlist Manager: Doubly Linked List Demo
This is a single-page web application (SPA) designed for a college project to visually demonstrate the Doubly Linked List data structure. It simulates a music playlist to showcase efficient bidirectional traversal (O(1) constant time) and circular list logic.

✨ Key Features & Concepts
Data Structure: Logical Doubly Linked List (simulated using JavaScript array indexing).

Traversal: Instant "Next Song" and "Previous Song" movement.

Design: Responsive interface using Tailwind CSS.

Mode: Runs in Local Simulation Mode (browser memory only) for reliable, error-free presentation.

🛠️ Technology Stack

HTML5 => Structure

JavaScript => Logic Engine & Traversal Algorithms

Tailwind CSS => Styling & Responsive Design

🚀 How to Run
Download: Save the index.html file.

Launch: Double-click the index.html file to open it in any web browser.

(Optional): For live reloading, use the Live Server extension in VS Code.

💡 Implementation Glimpse
The core logic uses index calculation to simulate the next pointer of a Doubly Linked List, including the wrap-around functionality:

// Function to simulate moving to the next node (O(1) concept)
function handleNextSong() {
    const currentIndex = playlist.findIndex(song => song.id === currentSongId);
    
    // Calculate the next index: If at the end, loop back to index 0.
    const nextIndex = (currentIndex >= 0 && currentIndex < playlist.length - 1) 
                        ? currentIndex + 1 
                        : 0; 
    
    if (playlist[nextIndex]) {
        setCurrentSong(playlist[nextIndex].id);
    }
}
