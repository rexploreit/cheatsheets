Disassemble all classes into a single .j file
`$ krak2 dis Some.jar -r --out j.j`

Open the `j.j` file with your favorite text editor to edit the java bytecode.

Create the new .jar file by assembling multiple classfiles from the single .j file
`$ krak2 asm --out Tampered.jar j.j`

For now, v2 does not pull the manifest or use it for reassembly so the jar file does not know the proper entry point
`$ java -cp Tampered.jar <entry>`
