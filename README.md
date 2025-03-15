Writing a Simple OS to target a raspberry pi using Rust.

References being used
 - https://os.phil-opp.com/freestanding-rust-binary/#introduction
 - https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials/tree/master


Target currently used for building:
 - aarch64-rusty_pi.json
  - excluded removal of SIMD features since -fp and -neon did not seem to be recognized
  - excluded addition of soft-float feature because it too doesn't seem to be recognized
  - did not set rust-abi to the aarch64_softfloat since soft-float couldn't be turned on (may need to revisit this later)
