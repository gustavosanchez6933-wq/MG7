# MG7
## Devlog
TreeofBirdsScript Code:

public class TreeOfBirds : MonoBehaviour
{
    [SerializeField] private GameObject[] _sparrows;
    [SerializeField] private float _interactiondistance;
    [SerializeField] private Transform _playerTransform;


    private void Update()
    {
        for (int i = 0; i < _sparrows.Length; i++) 
        {
            float distance = Vector3.Distance(_sparrows[i].transform.position, _playerTransform.position);
            if (distance <= _interactiondistance)
            {
                _sparrows[i].SetActive(true);
            }
        }
    }

}


1. First, I created public class Tree of Birds: Monobehvaior so I can add it the Tree Game Object. Then, I created an array: [SerializeField] private GameObject[] _sparrows; in order to add all the sparrows to the script except Sparrow_start. _Interactiondistance and _playerTransfrom was created to check the distance between both the bird and the player and tune how far they can interact. After that, I used an Update method to check the for loop every frame. In beginning of the for loop, int i checks to see how many sparrows there are before it stops. After that, I added  float distance = Vector3.Distance(_sparrows[i].transform.position, _playerTransform.position); to check the distance between the two game objects. Specifically, Vector3.Distance is used in order to calculate where the sparrows and the players are. Lastly, I used and if statement to tell the game that if the distance is less than or equal to interaction distance, then the sparrows array are set to activate.

## Open-Source Assets
- [Forest Nature Pack](https://kaylousberg.itch.io/kaykit-forest) - environment 3D models
- [Quirky Series](https://assetstore.unity.com/packages/3d/characters/animals/quirky-series-free-animals-pack-178235) - animal 3D models
