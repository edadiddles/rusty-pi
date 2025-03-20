Writing a Simple OS to target a raspberry pi using Rust.

References being used
 - https://os.phil-opp.com/freestanding-rust-binary/#introduction
 - https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials
 - https://wiki.osdev.org

Things to Reconsider:
 - remove spin dependency for own impl of mutex

OS Targets:
 - x86_64-rusty_pi.json (currently using to make progress)
  - x86_64 arch used by phil-opp tutorial
  - bootloader dependency supports x86_64 only
 - aarch64-rusty_pi.json (on hold)
  - excluded removal of SIMD features since -fp and -neon did not seem to be recognized
  - excluded addition of soft-float feature because it too doesn't seem to be recognized
  - did not set rust-abi to the aarch64_softfloat since soft-float couldn't be turned on (may need to revisit this later)
