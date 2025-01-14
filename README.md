<!DOCTYPE html>
<html lang="en">
<body>
    <h1><b>Deep Learning Setup Guide</b></h1>
    <h2>Deep Learning Setup Guide for MacBook Air M1</h2>
    <p>This guide outlines the steps to set up a deep learning environment on a MacBook Air M1 from scratch.</p>
    <h2>Step 1: Clean Up Existing Installations</h2>
    <p>Remove any existing Python installations and virtual environments:</p>
    <pre><code>brew uninstall --ignore-dependencies python
pip freeze > installed_packages.txt
pip uninstall -y -r installed_packages.txt
rm -rf ~/.virtualenvs
</code></pre>
    <p>If you had Mambaforge or Conda installed, remove them:</p>
    <pre><code>rm -rf ~/miniconda ~/anaconda3 ~/.condarc ~/.conda ~/.continuum
</code></pre>
    <h2>Step 2: Install Python 3.10</h2>
    <p>Install a compatible Python version:</p>
    <pre><code>brew install python@3.10
</code></pre>
    <p>Verify the installation:</p>
    <pre><code>python3.10 --version
</code></pre>
    <h2>Step 3: Set Up a Virtual Environment</h2>
    <p>Create and activate a new virtual environment:</p>
    <pre><code>python3.10 -m venv ~/deep_learning_env
source ~/deep_learning_env/bin/activate
</code></pre>
    <p>Upgrade pip and related tools:</p>
    <pre><code>pip install --upgrade pip setuptools wheel
</code></pre>
    <h2>Step 4: Install TensorFlow for M1</h2>
    <p>Install TensorFlow optimized for M1 hardware:</p>
    <pre><code>pip install tensorflow-macos tensorflow-metal
</code></pre>
    <p>Verify the installation:</p>
    <pre><code>python -c "import tensorflow as tf; print(tf.__version__); print(tf.config.list_physical_devices('GPU'))"
</code></pre>
    <h2>Step 5: Install Additional Libraries</h2>
    <p>Install commonly used libraries:</p>
    <pre><code>pip install numpy pandas matplotlib scikit-learn jupyterlab
</code></pre>
    <p>For computer vision:</p>
    <pre><code>pip install opencv-python Pillow
</code></pre>
    <p>For natural language processing:</p>
    <pre><code>pip install nltk spacy
</code></pre>
    <h2>Step 6: Test the Setup</h2>
    <p>Run the following script to confirm the setup:</p>
    <pre><code>import tensorflow as tf
import numpy as np

print("TensorFlow version:", tf.__version__)
print("Available GPUs:", tf.config.list_physical_devices('GPU'))

# Simple TensorFlow computation
a = tf.constant([[1, 2], [3, 4]])
b = tf.constant([[5, 6], [7, 8]])
print("Matrix multiplication result:", tf.matmul(a, b).numpy())
</code></pre>
    <h2>Step 7: Optional Tools</h2>
    <p>Install JupyterLab for interactive development:</p>
    <pre><code>pip install jupyterlab
jupyter lab
</code></pre>
    <p>Download and install <a href="https://code.visualstudio.com/">VS Code</a> for an advanced IDE.</p>
    <h2>Step 8: Best Practices</h2>
    <p>Always activate your virtual environment before working on projects:</p>
    <pre><code>source ~/deep_learning_env/bin/activate
</code></pre>
    <p>Use a <code>requirements.txt</code> file for dependency management:</p>
    <pre><code>pip freeze > requirements.txt
pip install -r requirements.txt
</code></pre>
<h2>Step 8: JupyterLab Shortcuts</h2>
    <h3>Command Mode Shortcuts</h3>
    <ul>
        <li><code>A</code>: Insert a new cell above</li>
        <li><code>B</code>: Insert a new cell below</li>
        <li><code>D, D</code>: Delete selected cell</li>
        <li><code>Z</code>: Undo cell deletion</li>
        <li><code>X</code>: Cut selected cell</li>
        <li><code>C</code>: Copy selected cell</li>
        <li><code>V</code>: Paste cell below</li>
        <li><code>Shift + V</code>: Paste cell above</li>
        <li><code>M</code>: Convert cell to Markdown</li>
        <li><code>Y</code>: Convert cell to code</li>
        <li><code>Shift + Enter</code>: Run cell and move to the next</li>
    </ul>
    <h3>Edit Mode Shortcuts</h3>
    <ul>
        <li><code>Ctrl + A</code>: Select all</li>
        <li><code>Ctrl + Z</code>: Undo</li>
        <li><code>Ctrl + Shift + Z</code>: Redo</li>
        <li><code>Ctrl + /</code>: Toggle comment for selected lines</li>
        <li><code>Tab</code>: Indent</li>
        <li><code>Shift + Tab</code>: Dedent</li>
        <li><code>Ctrl + Space</code>: Trigger code completion</li>
        <li><code>Ctrl + Shift + -</code>: Split the current cell at the cursor</li>
    </ul>
    <h3>General Shortcuts</h3>
    <ul>
        <li><code>Shift + Esc</code>: Exit edit mode and focus on the cell</li>
        <li><code>Ctrl + S</code>: Save notebook</li>
        <li><code>0, 0</code>: Restart kernel</li>
        <li><code>F</code>: Open the command palette</li>
    </ul>
    <h2>Step 9: Best Practices</h2>
    <p>Always activate your virtual environment before working on projects:</p>
    <pre><code>source ~/deep_learning_env/bin/activate
</code></pre>
    <p>Use a <code>requirements.txt</code> file for dependency management:</p>
    <pre><code>pip freeze > requirements.txt
pip install -r requirements.txt
</code></pre>
    <h2>Conclusion</h2>
    <p>You are now ready to start working on deep learning projects on your MacBook Air M1!</p>
    <h2>Conclusion</h2>
    <p>You are now ready to start working on deep learning projects on your MacBook Air M1!</p>
</body>
</html>
