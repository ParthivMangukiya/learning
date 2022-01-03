# Random Notes/Understandings

- Dynamically Sized Types
	- https://doc.rust-lang.org/nomicon/exotic-sizes.html
	- There are two major DSTs exposed by the language:
			- trait objects: dyn MyTrait
			- slices: [T], str, and others
	- DSTs are not normal types. Because they lack a statically known size, these types can only exist behind a pointer.
- Reference to a trait type is trait object
- In memory, trait object is fat pointer
	- data pointer - poiter to the value
	- vtable pointer - vtable is generated at compiletime and share by all objects of the same type
- Rust can automatically convert ordinary references to trait object, Rust can also do the same for smart pointers rc and box.
	- convert ` let mut buffer: Vec<u8>; let w: &mut dyn Write = &mut buffer;`
- Rust does not have concreate type for clousures. Rust defines three traits Fn, FnOnce, FnMut
	- Rust internally creates struct for the clusures and implements the appropriate traits on the sturct
	- **“You compile the compiler with the compiler, then you compile the compiler with the compiler again, so that it doesn’t have the bugs that it has”.**
 - `&` and `&mut` is shared and exclusive references, these guarantees are enforced by rust compiler, whereas, *const and *mut are raw pointers, there are no guarantees by compiler so unsafe
 -



