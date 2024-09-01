# imagechoose
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      body {
        background: #2f2f2f;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
      }
      .image-container {
        height: 200px;
        width: 200px;
        border: 5px solid #f1c40f;
        border-radius:50%;
        overflow:hidden;
      }


      .image-container img {
        height: 100%;
        width: 100%;
      }
      .image-prev {
        margin-top: 3rem;
        text-align: center;
      }
      #userimage {
        display: none;
      }
      #imagelabel {
        color: #fff;
        background-image: linear-gradient(45deg, #fbaf1d 50%, transparent 50%);
        background-position: 100%;
        background-size: 400%;
        background-color: transparent;
        border: 2px solid #fbaf1d;
        border-radius: 0.6em;
        cursor: pointer;
        font-size: 1rem;
        padding: 1.2em 2.8em;
        text-transform: uppercase;
        font-family: "Montserrat", sans-serif;
        font-weight: 700;
        transition: background 300ms ease-in-out;
      }
      #imagelabel:hover,
      #imagelabel:focus {
        color: #fff;
        outline: 0;
        background-position: 0;
      }
    </style>
  </head>
  <body>
    <div class="image-container">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/7/7c/Profile_avatar_placeholder_large.png?20150327203541"
        alt="" id="preview"
      />
    </div>
    <div class="image-prev">
      <label for="userimage" id="imagelabel">choose image</label> <br />
      <input type="file" name="" id="userimage" onchange="showPreview(this)" />
    </div>
<script>
    function showPreview(input) {
        // Get the file object from the input element.
        const file = input.files[0];

        // Get the image element by its ID
        let image = document.getElementById("preview");
            
        // Use URL.createObjectURL to create a blob URL for the selected file
        const blobUrl = URL.createObjectURL(file);

       // Set the 'src' attribute of the image element to the blob URL
      image.src = blobUrl;

       

        
      }
    </script>
  </body>
</html>
