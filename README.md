# mHSP2

**mHSP2** is the HSPF variant used in the [**pyHS2MF6**](https://nmartin198.github.io/pyHS2MF6/)
integrated hydrologic model. It has been separated out from **pyHS2MF6** 
to facilitate standalone use of this program.

**mHSP2** is a port of [HSPsquared](https://github.com/respec/HSPsquared) created 
specifically for coupled simulation with MODFLOW 6.
[HSPsquared](https://github.com/respec/HSPsquared) is an HSPF variant 
that was rewritten in pure Python. **mHSP2** only provides the water 
movement and storage capabilities of [HSPsquared](https://github.com/respec/HSPsquared).

The main difference between **mHSP2** and [HSPsquared](https://github.com/respec/HSPsquared) 
is that **mHSP2** was created with the simulation time loop as 
the main simulation loop to facilitate dynamic coupling to MODFLOW 6. 
HSPF-variants traditionally use an operating module instance loop that 
is executed in routing order as the main simulation loop. This approach 
requires that the time simulation loop be executed for each operating 
module instance.

[**Additional details**](https://nmartin198.github.io/pyHS2MF6/mHSP2.html)


## Getting Started

The Python source code for **mHSP2** is in the [*src*](https://github.com/nmartin198/mHSP2/tree/main/src) 
directory. The best way to start is to go through the 
[HSPF Standalone Example Model](https://nmartin198.github.io/pyHS2MF6/cs_sa_HSPF.html) 
in the **pyHS2MF6** documentation and run that model and verify that obtain 
similar results.

The next step would be to use the [example model](https://github.com/nmartin198/mHSP2/tree/main/example_input) 
included in this repository as a second example case.

There is also a utility [Jupyter Notebook](https://github.com/nmartin198/mHSP2/tree/main/jupyter_notebooks/Conv_pyHSPF_HSP2.ipynb) 
included in this repository that provides an example of going 
from the traditional HSPF inputs of UCI and WDM files to the HDF5 
input file used by **mHSP2**.

## Contributing

The author is happy to accept contributions to the project. It might be easiest to contact me prior to starting your contribution in case there are any initial suggestions or direction that I can provide.

The general procedure for contributing is as follows.

- Fork the project
- Make your changes
- Submit a pull request
    - It is important to have a conversation when opening a pull request. Describe your change and why it should be accepted.

## Author

* **Nick Martin** nmartin@swri.org

## License

This project is licensed under the GNU Affero General Public License v.3.0 - see the [LICENSE](LICENSE) file for details.
