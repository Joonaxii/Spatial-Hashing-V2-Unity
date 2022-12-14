# Spatial Hashing V2 for Collision (Unity, C#)
A new implementation of a spatial hash grid used for collision detection in Unity. Around a year ago, I made an iteration on my very old spatial hash grid I used for 2D collision detection. That iteration was made for a presentation for school. 
This new version aims to address some issues I ran into with the old implementation, or just couldn't get done in time for the assignment, while also adding some new features.

##Features
The core idea remains the same, there's a grid that stores objects, or more specifically indices of objects which can then be used with collision detection to speed up collision checks. However, this new version aims to increase the scale of the grid by introducing "proper" chunks where the chunks are fixed size, but the amount of chunks can be variable. This does mean that this implementation isn't a 100% exactly how one would implement a spatial hash grid, but it uses the same core principals as a typical spatial hash grid.

This implementation also attempts to address the huge memory allocations the previous version had by using an "Analysis" phase which checks allocates/deallocates the index buffer.

## Notes

This project relies quite heavily on C#'s <b>Span\<T\></b> & as such, at least for the time being is only supported in versions of Unity that support <b>Span\<T\></b>.
The specific <b>Unity</b> version used in this project is <b>Unity 2021.3.15f1</b>

The implementation is in very early development, so the project is seemingly empty for some time while I develop the implementation further.
I probably will implement this in my own "engine" as well later down the line, but for now I'm testing my ideas out in an environment I'm more familiar with. 
