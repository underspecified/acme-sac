# Guidelines for Acme-SAC maintenance. #

  1. **Existing functionality before new features.** Functionality that exists today should be written in code that is clear, correct, compact, documented (man pages), well tested and run solidly on all platforms.
  1. **Inferno principles before new features: Emu and jit running well on more platforms.** The emu should be ported with working JIT and work well on as many platforms as possible.
  1. **Eat your own dog food.** Live in the system before changing it. Maintainers should use Acme SAC daily.
  1. **Stick to the original design: The core of the system should reach an asymptotic limit** Make the Knuth offer to people who find bugs. Define the core: the VM, limbo, acme, shell, sys.m, parts of namespace.
  1. **Expand outside the core.** Have extension points outside the core to extend the system. Script languages, fs interfaces.
  1. **Outside the core go crazy.** Use inferno-lab to experiment, change anything, go crazy.